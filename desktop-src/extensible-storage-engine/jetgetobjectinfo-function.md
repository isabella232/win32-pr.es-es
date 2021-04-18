---
description: 'Más información acerca de: JetGetObjectInfo (función)'
title: Función JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716164"
---
# <a name="jetgetobjectinfo-function"></a>Función JetGetObjectInfo


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetobjectinfo-function"></a>Función JetGetObjectInfo

La función **JetGetObjectInfo** recupera información acerca de los objetos de base de datos. Actualmente, solo se admiten tablas. [JetGetTableInfo](./jetgettableinfo-function.md) se puede usar para obtener más información que **JetGetObjectInfo**.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar.

*DBID*

Base de datos de la que se recupera la información.

*objtyp*

Objetos que contienen información que se va a recuperar. Actualmente, solo se admiten JET_objtypNil y JET_objtypTable, ambos de los cuales se comportan exactamente igual. Solo se recuperarán las tablas.

*szContainerName*

Este parámetro está reservado para un uso futuro y pasa **null**. Nombre de los tipos de objetos sobre los que se va a recuperar información.

*szObjectName*

Nombre del objeto que contiene la información que se va a recuperar. Cuando *InfoLevel* usa las opciones JET_ObjInfoList o JET_ObjInfoListNoStats para recuperar una lista de todos los objetos, este valor debe ser **null** o una cadena vacía.

Actualmente solo se admiten nombres de tabla.

*pvResult*

Puntero a un búfer que recibe la información especificada.

El tamaño del búfer, en bytes, se pasa en *cbMax*. En caso de error, el contenido de *pvResult* no está definido.

La información que se almacena en *pvResult* depende de *InfoLevel*.

*cbMax*

Tamaño, en bytes, del búfer pasado en *pvResult*.

*InfoLevel*

Especifica el tipo de información que se va a recuperar para el objeto especificado. Afecta al modo en que se interpreta *pvResult* .

Las siguientes opciones están disponibles para establecerse para este parámetro.

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
<td><p>JET_ObjInfo</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</p>
<p>La estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> se rellena con información relacionada con el objeto denominado en <em>szObjectName</em>.</p>
<p>Si el autor de la llamada no desea conocer el número de registros y páginas del objeto, considere la posibilidad de usar JET_ObjInfoNoStats nivel de información, que podría ser más rápido, ya que no se incluyen las estadísticas.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoList</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Se recupera información sobre todos los objetos. Se creará una tabla temporal y la información necesaria para recorrer la tabla temporal se describe en la estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Para obtener más información, vea <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Si el autor de la llamada no desea conocer el número de registros y páginas del objeto, considere la posibilidad de usar JET_ObjInfoListNoStats, lo que podría ser más rápido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoListACM</p></td>
<td><p>En desuso y no se admite actualmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoListNoStats</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Se recupera información sobre todos los objetos. Se creará una tabla temporal y la información necesaria para recorrer la tabla temporal se describe en la estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Para obtener más información, vea <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats es idéntica a JET_ObjInfoList, salvo que las columnas que informan del número de registros (<em>columnidcRecord</em>) y las páginas (<em>columnidcPage</em>) no se actualizarán.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoMax</p></td>
<td><p><em>pvResult</em> se interpreta como <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. El tamaño máximo del objeto está en páginas. Actualmente solo se devolverán las tablas.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoNoStats</p></td>
<td><p><em>pvResult</em> se interpreta como <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Solo se recuperará información sobre el objeto proporcionado en <em>szObjectName</em> .</p>
<p>La estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> se rellenará con información relativa al objeto denominado en <em>szObjectName</em>.</p>
<p>JET_ObjInfoNoStats es idéntica a JET_ObjInfo, salvo que los campos que informan del número de registros y páginas se establecen en cero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoRulesLoaded</p></td>
<td><p>En desuso y no se admite actualmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoSysTabCursor</p></td>
<td><p>En desuso y no se admite actualmente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoSysTabReadOnly</p></td>
<td><p>En desuso y no se admite actualmente.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>El tamaño del búfer proporcionado en <em>cbMax</em> era demasiado pequeño para contener la información deseada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Se proporcionó un nombre no válido en <em>szObjectName</em> o <em>szContainerName</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se proporcionó un parámetro incorrecto. Es posible que se haya pasado un nivel no válido a <em>InfoLevel</em>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Si **JetGetObjectInfo** crea correctamente una tabla temporal (por ejemplo, JET_ObjInfoList o JET_ObjInfoNoStats), el autor de la llamada es responsable de cerrar la tabla temporal con [JetCloseTable](./jetclosetable-function.md).

**JetGetObjectInfo** actualmente solo admite la recuperación de información sobre tablas.

#### <a name="requirements"></a>Requisitos

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
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetGetObjectInfoW</strong> (Unicode) y <strong>JetGetObjectInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
