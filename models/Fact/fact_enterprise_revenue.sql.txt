SELECT
    industry_name_ANZSIC,
    year,
    SUM(value) AS total_revenue
FROM {{ ref('stg_enterprise_survey') }}
WHERE variable = 'Sales, government funding, grants and subsidies'
GROUP BY industry_name_ANZSIC, year
