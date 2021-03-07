# mysql_sys.memory_global_total-

SELECT 
    FORMAT_BYTES(SUM(`performance_schema`.`memory_summary_global_by_event_name`.`CURRENT_NUMBER_OF_BYTES_USED`)) AS `total_allocated`
FROM
    `performance_schema`.`memory_summary_global_by_event_name`
