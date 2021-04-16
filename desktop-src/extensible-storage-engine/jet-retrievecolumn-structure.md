---
description: 'Más información acerca de: estructura de JET_RETRIEVECOLUMN'
title: Estructura de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705757"
---
# <a name="jet_retrievecolumn-structure"></a>Estructura de JET_RETRIEVECOLUMN


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_retrievecolumn-structure"></a>Estructura de JET_RETRIEVECOLUMN

La estructura **JET_RETRIEVECOLUMN** contiene los parámetros de entrada y salida de [JetRetrieveColumns](./jetretrievecolumns-function.md). Los campos de la estructura describen qué valor de columna se va a recuperar, cómo se recupera y dónde se guardan los resultados.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Miembros

**columnid**

Identificador de columna para la columna que se va a recuperar.

**pvData**

Un puntero para empezar a almacenar los datos que se recuperan del valor de la columna.

**cbData**

Tamaño de la asignación a partir de **pvData**, en bytes. La operación de recuperación de columna no almacenará más datos en **pvData** que **cbData**.

**cbActual**

Tamaño, en bytes, de los datos recuperados por una operación de recuperación de columna.

**grbit**

Grupo de bits que contiene las opciones para la recuperación de columnas, que incluyen cero o más de los valores siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Recupera el valor modificado en lugar del valor original. Si el valor no se ha modificado, se recupera el valor original. De esta manera, se puede recuperar un valor que todavía no se ha insertado o actualizado cuando se inserta o actualiza un registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Recupera los valores de columna del índice sin tener acceso al registro, si es posible. De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice. En los casos en los que no se puede recuperar el valor de la columna original del índice debido a las transformaciones irreversibles o al truncamiento de los datos, se obtendrá acceso al registro y se recuperarán los datos de la forma habitual. Se trata de una opción de rendimiento y solo se debe especificar cuando es probable que se pueda recuperar el valor de la columna del índice. Esta opción no se debe especificar si el índice actual es el índice clúster, ya que las entradas de índice para el índice agrupado, o principal, son los propios registros. No se puede establecer este bit si también se establece JET_bitRetrieveFromPrimaryBookmark.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Recupera los valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece en el índice principal y en el índice actual. Esta opción no se debe especificar si el índice actual es el índice clúster o principal. No se puede establecer este bit si también se establece JET_bitRetrieveFromIndex.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Recupera el número de secuencia de un valor de columna de varios valores en pretinfo- &gt; itagSequence. A menudo, el campo itagSequence se usa como entrada para recuperar valores de columna con varios valores de un registro. Sin embargo, cuando se recuperan valores de un índice, también es posible asociar la entrada de índice con un número de secuencia determinado y recuperar también este número de secuencia. Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ bitRetrieveNull</p></td>
<td><p>Recupera los valores NULL de la columna con varios valores. Si no se especifica esta opción, se omitirán automáticamente los valores NULL de las columnas con varios valores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Hace que se devuelva un valor NULL cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro. Esta opción solo afecta a las columnas con varios valores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</p></td>
</tr>
</tbody>
</table>


**ibLongValue**

Desplazamiento al primer byte que se va a recuperar de una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Número de secuencia de los valores contenidos en una columna con varios valores. **itagSequence** aquí en el **JET_RETRIEVECOLUMN** puede ser 0. Si el valor de **itagSequence** es 0, se devuelve el número de instancias de una columna con varios valores en lugar de datos de columna. No se puede usar un valor de **itagSequence** de 0 en llamadas a [JetRetrieveColumn](./jetretrievecolumn-function.md).

**columnidNextTagged**

El **columnid** de la columna etiquetada, con varios valores o disperso cuando se recuperan todas las columnas etiquetadas pasando 0 como **columnid** a [JetRetrieveColumn](./jetretrievecolumn-function.md).

**ERR**

Códigos de error y advertencias devueltos por la recuperación de la columna.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
