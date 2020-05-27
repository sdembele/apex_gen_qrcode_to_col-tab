<p>
Use this plugin to generate <span style="color: #B8622A;"><strong>QRCODE</strong></span>&nbsp;</p>
<p>Which can be stored either in one:</p>
<ul>
<li><strong><span style="color: #B8622A;">Collection</span></strong></li>
<li><span style="color: #B8622A;"><strong>Table</strong></span> (by <em>insertion</em> or <em>modification</em>)</li>
</ul>
<p>The data to generate comes from the sql request that you will provide</p>
<p>For this example the following query is used:</p>
<code><span style="color: #B8622A;">select rownum   as qr_id, -- represente table pk id<br/>
       case rownum<br/>
       when 1 then 'Welcome'<br/>
       when 2 then 'Bienvenue'<br/>
       when 3 then 'مرحبا بك'<br/> 
       when 4 then 'Bienvenido' <br/>
       else 'Have a nice day' <br/>
       end      as  qr_text<br/>
from dual<br/>
connect by level < 6
</span></code>
<p><strong><span style="text-decoration: underline;">The parameters of this plugin are:</span></strong></p>
<div class="t-Report-tableWrap">
<table class="qr_table">
<thead>
<tr>
<td>Parameters</td>
<td>Description</td>
</tr>
</thead>
<tbody>
<tr>
<td>The SQL Query</td>
<td>Specify the SQL query</td>
</tr>
<tr>
<td>
<p>The Storage type</p>
</td>
<td>Specify if you want to store the result in a collection or in a table</td>
</tr>
<tr>
<td>The DML Operation</td>
<td>Specifiy if you want to insert the result to table or update each lines reterning by the query.<br/> The <strong>QR_ID</strong> represent the PK id of your table</td>
</tr>
<tr>
<td>
<p>The Table Name</p>
</td>
<td>In case of collection this name will be used for the name of the collection,<br/> and if the storage type is table then the DML operations will be based on it</td>
</tr>
<tr>
<td>
<p>The PK Column</p>
</td>
<td>Identified the PK column</td>
</tr>
<tr>
<td>The Clob Column</td>
<td>identify the clob colomn which will contain the svg representation of qrcode</td>
</tr>
<tr>
<td>
<p>Qrcode Colors</p>
</td>
<td>Specify the qrcode's black and white color</td>
</tr>
</tbody>
</table>
</div>
<p>&nbsp;</p>
