SELECT
    year::INT AS year,
    industry_code_ANZSIC,
    industry_name_ANZSIC,
    rme_size_grp,
    variable,
    value::FLOAT AS value,
    unit
FROM {{ source('raw_schema', 'enterprise_survey') }}
