---
description: El lenguaje de consulta de WMI (WQL) es un subconjunto del American National Standards Institute Lenguaje de consulta estructurado (ANSI SQL)&8212; con cambios semánticos \# menores. En la tabla siguiente se enumeran las palabras clave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL para WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e2c80473874390851e81a5f2acebcd6d7e1497
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626761"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL para WMI)

El lenguaje de consulta de WMI (WQL) es un subconjunto del American National Standards Institute Lenguaje de consulta estructurado (ANSI SQL) con cambios semánticos menores. En la tabla siguiente se enumeran las palabras clave WQL.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Palabra clave WQL</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>y<br/></td>
<td>Combina dos expresiones booleanas y devuelve <strong>TRUE</strong> cuando ambas expresiones son <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASOCIADORES DE</a></td>
<td>Recupera todas las instancias asociadas a una instancia de origen.<br/> Use esta instrucción con consultas de esquema y consultas de datos.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Hace referencia a la clase del objeto en una consulta.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Especifica la clase que contiene las propiedades enumeradas en una instrucción SELECT. Windows Instrumental de administración (WMI) admite consultas de datos de una sola clase a la vez.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Cláusula GROUP</a></td>
<td>Hace que WMI genere una notificación para representar un grupo de eventos.<br/> Use esta cláusula con consultas de eventos.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtra los eventos que se reciben durante el intervalo de agrupación especificado en la <a href="within-clause.md">cláusula WITHIN</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Operador de comparación utilizado con NOT y <strong>NULL.</strong> La sintaxis de esta instrucción es la siguiente:<br/> IS [NOT] <strong>NULL</strong><br/> (donde NOT es opcional)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operador que aplica una consulta a las subclases de una clase especificada. Para obtener más información, vea <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>y <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Se usa en las consultas <a href="references-of-statement.md">REFERENCES OF</a> y <a href="associators-of-statement.md">ASSOCIATORS OF</a> para asegurarse de que las instancias resultantes solo se rellenan con las claves de las instancias, lo que reduce la sobrecarga de la llamada.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operador que determina si una cadena de caracteres determinada coincide o no con un patrón especificado.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Operador de comparación que usa en una consulta SELECT de WQL, por ejemplo:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indica que un objeto no tiene un valor asignado explícitamente. <strong>NULL</strong> no es equivalente a cero (0) o en blanco.<br/></td>
</tr>
<tr class="odd">
<td>O BIEN<br/></td>
<td>Combina dos condiciones.<br/> Cuando se usa más de un operador lógico en una instrucción , los operadores OR se evalúan después de los operadores AND.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">REFERENCIAS DE</a></td>
<td>Recupera todas las instancias de asociación que hacen referencia a una instancia de origen específica. Use esta instrucción con consultas de esquema y datos. La <a href="references-of-statement.md">instrucción REFERENCES OF</a> es similar a la instrucción <a href="associators-of-statement.md">ASSOCIATORS OF.</a> Sin embargo, no recupera instancias de punto de conexión; recupera las instancias de asociación.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Especifica las propiedades que se usan en una consulta.<br/> Para obtener más información, vea <a href="select-statement-for-data-queries.md">Instrucción SELECT</a>para consultas de datos , Instrucción SELECT para consultas <a href="select-statement-for-event-queries.md">de</a>eventos o Instrucción SELECT para consultas <a href="select-statement-for-schema-queries.md">de esquema</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Operador booleano que se evalúa como -1 (menos uno).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Limita el ámbito de una consulta de datos, eventos o esquemas.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Especifica un intervalo de sondeo o agrupación.<br/> Use esta cláusula con consultas de eventos.<br/></td>
</tr>
<tr class="odd">
<td>false<br/></td>
<td>Operador booleano que se evalúa como 0 (cero).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> El uso de una palabra clave WQL como nombre de objeto puede dar lugar a una consulta que no se puede analizar incluso cuando la consulta se compila sin errores.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> <dt>

[Formatos de fecha admitidos por WQL](wql-supported-date-formats.md)
</dt> <dt>

[Formatos de hora compatibles con WQL](wql-supported-time-formats.md)
</dt> </dl>

 

 




