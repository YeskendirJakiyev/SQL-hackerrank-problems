Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

Input Format

The STATION table is described as follows:

<table>
<thead>
<tr>
<th>Field</th>
<th>Type</th>
</tr>
</thead>
<tbody>
<tr>
<td>ID</td>
<td>NUMBER</td>
</tr>
<tr>
<td>NAME</td>
<td>VARCHAR2(17)</td>
</tr>
<tr>
<td>COUNTRY CODE</td>
<td>VARCHAR2(3)</td>
</tr>
<tr>
<td>DISTRICT</td>
<td>VARCHAR2(20)</td>
</tr>
<tr>
<td>POPULATION</td>
<td>NUMBER</td>
</tr>
</tbody>
</table>

where LAT_N is the northern latitude and LONG_W is the western longitude.

<p><strong>Solution</strong></p>

<pre>
SELECT CITY
FROM STATION
WHERE
    CITY NOT LIKE "A%"
    AND CITY NOT LIKE "E%"
    AND CITY NOT LIKE "I%"
    AND CITY NOT LIKE "O%"
    AND CITY NOT LIKE "U%"
GROUP BY CITY
<pre>

