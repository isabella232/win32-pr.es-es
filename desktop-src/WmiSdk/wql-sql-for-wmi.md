---
description: El lenguaje de consulta de WMI (WQL) es un subconjunto del Lenguaje de consulta estructurado de American National Standards Institute (ANSI SQL) &\# 8212; con cambios semánticos menores. En la tabla siguiente se enumeran las palabras clave de WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL para WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276244"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL para WMI)

El lenguaje de consulta de WMI (WQL) es un subconjunto del Lenguaje de consulta estructurado de American National Standards Institute (ANSI SQL) con cambios semánticos menores. En la tabla siguiente se enumeran las palabras clave de WQL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Combina dos expresiones booleanas y devuelve <strong>true</strong> cuando ambas expresiones son <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOCIATORS OF</a></td>
<td>Recupera todas las instancias de asociadas a una instancia de de origen.<br/> Use esta instrucción con consultas de esquema y consultas de datos.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Hace referencia a la clase del objeto en una consulta.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Especifica la clase que contiene las propiedades enumeradas en una instrucción SELECT. Instrumental de administración de Windows (WMI) admite consultas de datos de una sola clase a la vez.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">GROUP (cláusula)</a></td>
<td>Hace que WMI genere una notificación para representar un grupo de eventos.<br/> Use esta cláusula con consultas de eventos.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtra los eventos que se reciben durante el intervalo de agrupación especificado en la <a href="within-clause.md">cláusula Within</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Operador de comparación utilizado con NOT y <strong>null</strong>. La sintaxis de esta instrucción es la siguiente:<br/> IS [NOT] <strong>null</strong><br/> (donde no es opcional)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operador que aplica una consulta a las subclases de una clase especificada. Para obtener más información, vea <a href="isa-operator-for-event-queries.md">operador ISA para consultas de eventos</a>, <a href="isa-operator-for-data-queries.md">operador ISA para consultas de datos</a>y <a href="isa-operator-for-schema-queries.md">operador ISA para consultas de esquema</a>.<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Se utiliza en <a href="references-of-statement.md">referencias de</a> y <a href="associators-of-statement.md">asociadores de</a> consultas para asegurarse de que las instancias resultantes solo se rellenan con las claves de las instancias, lo que reduce la sobrecarga de la llamada.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operador que determina si una cadena de caracteres determinada coincide con un patrón especificado.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Operador de comparación que utiliza en una consulta WQL SELECT, por ejemplo:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indica que un objeto no tiene un valor asignado explícitamente. <strong>Null</strong> no es equivalente a cero (0) o en blanco.<br/></td>
</tr>
<tr class="odd">
<td>O BIEN<br/></td>
<td>Combina dos condiciones.<br/> Cuando se utiliza más de un operador lógico en una instrucción, los operadores OR se evalúan después de los operadores y.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">REFERENCIAS DE</a></td>
<td>Recupera todas las instancias de asociación que hacen referencia a una instancia de origen concreta. Use esta instrucción con consultas de esquema y de datos. La instrucción <a href="references-of-statement.md">References de</a> es similar a la instrucción <a href="associators-of-statement.md">ASSOCIATORS of</a> . Sin embargo, no recupera las instancias de extremo; Recupera las instancias de asociación.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Especifica las propiedades que se utilizan en una consulta.<br/> Para obtener más información, vea <a href="select-statement-for-data-queries.md">instrucción SELECT para consultas de datos</a>, <a href="select-statement-for-event-queries.md">instrucción SELECT para consultas de eventos</a>o <a href="select-statement-for-schema-queries.md">instrucción SELECT para consultas de esquema</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Operador booleano que se evalúa como-1 (menos uno).<br/></td>
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

[WQL: formatos de fecha admitidos](wql-supported-date-formats.md)
</dt> <dt>

[WQL: formatos de hora compatibles](wql-supported-time-formats.md)
</dt> </dl>

 

 




