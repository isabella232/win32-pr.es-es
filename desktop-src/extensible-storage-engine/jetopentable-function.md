---
description: 'Más información acerca de: JetOpenTable (función)'
title: Función JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808431"
---
# <a name="jetopentable-function"></a>Función JetOpenTable


_**Se aplica a:** Windows | Windows Server_

## <a name="jetopentable-function"></a>Función JetOpenTable

La función **JetOpenTable** abre un cursor en una tabla creada anteriormente.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar.

*DBID*

Identificador de base de datos que se va a usar para buscar la tabla.

*szTableName*

Nombre de la tabla que se va a abrir.

*pvParameters*

En desuso. Se establece en **null**.

*cbParameters*

En desuso. Se establece en 0 (cero).

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

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
<td><p>JET_bitTableDenyRead</p></td>
<td><p>Otra sesión de base de datos no puede abrir la tabla para acceso de lectura.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>No se puede abrir la tabla para acceso de escritura en otra sesión de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>No almacene en caché las páginas de esta tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>Permite la modificación de DDL en las tablas marcadas como FixedDDL. Esta opción debe usarse con la opción JET_bitTableDenyRead.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>Proporciona una sugerencia que indica que la tabla probablemente no está en la caché del búfer y que la lectura previa puede ser beneficiosa para el rendimiento.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>Solicita acceso de solo lectura a la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>La tabla se debe capturar de forma muy agresiva desde el disco, ya que la aplicación la examinará secuencialmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>Solicita acceso de escritura a la tabla.</p></td>
</tr>
</tbody>
</table>


*ptableid*

Si se ejecuta correctamente, apunta al identificador de la tabla. En caso de error, el contenido de *ptableid* no está definido.

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
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>DBID</em> no es un identificador de base de datos válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Se pasó una combinación incorrecta de <em>grbit</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>El nombre proporcionado en <em>szTableName</em> no es válido.</p>
<p>Para obtener más información sobre los nombres de tabla válidos, vea el parámetro <em>szTableName</em> en <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Se intentó abrir una tabla que no existe en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Consulte la sección Comentarios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>Otra operación de base de datos está utilizando la tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Una advertencia no grave que indica que el sistema está usando la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>La tabla está bloqueada por otra operación de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Se intentó abrir demasiadas tablas únicas a la vez. Consulte la sección Comentarios.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Las tablas abiertas con **JetOpenTable** normalmente se deben cerrar con [JetCloseTable](./jetclosetable-function.md). La excepción a esta regla se produce cuando se llama a **JetOpenTable** en una transacción y se revierte la transacción (con [JetRollback](./jetrollback-function.md)). Cuando se revierte una transacción, la tabla se cierra automáticamente. En este caso, es un error cerrar la tabla con [JetCloseTable](./jetclosetable-function.md).

Es válido abrir tablas del sistema con **JetOpenTable** (por ejemplo, MSysObjects, MSysUnicodeFixup). El esquema de las tablas del sistema puede cambiar, por lo que no se recomienda el acceso a las tablas del sistema. El número de tablas únicas que se pueden abrir simultáneamente se ve afectado directamente por *JET_paramMaxOpenTables*. Si la tabla está abierta actualmente, se creará un nuevo cursor en la tabla. Los recursos de cursor se configuran mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxCursors*. Consulte también [JetDupCursor](./jetdupcursor-function.md).

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
<td><p>Se implementa como <strong>JetOpenTableW</strong> (Unicode) y <strong>JetOpenTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros de recursos](./resource-parameters.md)
