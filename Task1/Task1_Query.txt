SELECT
  d.NAME AS "DEPT_NAME",
  AVG(s.`AMT (USD)`) AS "AVG_MONTHLY_SALARY (USD)"
FROM
  Salaries s,
  Employees e,
  Departments d
WHERE
  e.id = s.EMP_ID
  AND d.ID = e.`DEPT ID`
GROUP BY
  d.Name ORDER BY AVG(s.`AMT (USD)`) DESC
LIMIT 3;
