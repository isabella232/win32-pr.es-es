---
description: 'Más información sobre: JetOpenTable (Función)'
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
ms.openlocfilehash: 7a288e3e1a625106c72f57125eea8a4219555f86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887260"
---
# <a name="jetopentable-function"></a>Función JetOpenTable


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopentable-function"></a>Función JetOpenTable

La **función JetOpenTable** abre un cursor en una tabla creada anteriormente.

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

Contexto de sesión de base de datos que se usará.

*Dbid*

Identificador de base de datos que se usará para buscar la tabla.

*szTableName*

Nombre de la tabla que se abrirá.

*pvParameters*

En desuso. Se establece en **NULL.**

*cbParameters*

En desuso. Establezca en 0 (cero).

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableDenyRead</p> | <p>Otra sesión de base de datos no puede abrir la tabla para el acceso de lectura.</p> | 
| <p>JET_bitTableDenyWrite</p> | <p>Otra sesión de base de datos no puede abrir la tabla para el acceso de escritura.</p> | 
| <p>JET_bitTableNoCache</p> | <p>No almacenar en caché las páginas de esta tabla.</p> | 
| <p>JET_bitTablePermitDDL</p> | <p>Permite la modificación de DDL en tablas marcadas como FixedDDL. Esta opción debe usarse con la JET_bitTableDenyRead predeterminada.</p> | 
| <p>JET_bitTablePreread</p> | <p>Proporciona una sugerencia de que la tabla probablemente no esté en la caché del búfer y que la lectura previa puede ser beneficiosa para el rendimiento.</p> | 
| <p>JET_bitTableReadOnly</p> | <p>Solicita acceso de solo lectura a la tabla.</p> | 
| <p>JET_bitTableSequential</p> | <p>La tabla debe tener una captura previa muy agresiva del disco porque la aplicación la examinará secuencialmente.</p> | 
| <p>JET_bitTableUpdatable</p> | <p>Solicita acceso de escritura a la tabla.</p> | 



*ptableid*

Si se ejecuta correctamente, apunta al identificador de la tabla. En caso de error, el contenido *de ptableid* no está definido.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p><em>dbid no</em> es un identificador de base de datos válido.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Se pasó una combinación no <em>correcta de grbit.</em></p> | 
| <p>JET_errInvalidName</p> | <p>El nombre especificado en <em>szTableName</em> no es válido.</p><p>Para obtener más información sobre los nombres de tabla válidos, vea el <em>parámetro szTableName</em> <a href="gg269210(v=exchg.10).md">en JetCreateTable</a>.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Se intentó abrir una tabla que no existe en la base de datos.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Consulte la sección Comentarios.</p> | 
| <p>JET_errTableInUse</p> | <p>Otra operación de base de datos está utilizando la tabla.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Una advertencia nofatal que indica que el sistema está utilizando la tabla.</p> | 
| <p>JET_errTableLocked</p> | <p>Otra operación de base de datos bloquea la tabla.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Se intentó abrir demasiadas tablas únicas a la vez. Consulte la sección Comentarios.</p> | 



#### <a name="remarks"></a>Observaciones

Las tablas abiertas **con JetOpenTable** normalmente deben cerrarse [con JetCloseTable.](./jetclosetable-function.md) La excepción a esta regla se produce cuando se llama a **JetOpenTable** en una transacción y la transacción se revierte [(con JetRollback).](./jetrollback-function.md) Al revertir una transacción, la tabla se cierra automáticamente. En este caso, es un error cerrar la tabla con [JetCloseTable](./jetclosetable-function.md).

Es legal abrir tablas del sistema con **JetOpenTable** (por ejemplo, MSysObjects, MSysUnicodeFixup). El esquema de las tablas del sistema puede cambiar, por lo que no se recomienda acceder a las tablas del sistema. El número de tablas únicas que se pueden abrir simultáneamente se ve afectado directamente por *JET_paramMaxOpenTables*. Si la tabla está abierta actualmente, se creará un nuevo cursor en la tabla. Los recursos de cursor se configuran [mediante JetSetSystemParameter](./jetsetsystemparameter-function.md) *con JET_paramMaxCursors*. Consulte también [JetDupCursor](./jetdupcursor-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetOpenTableW</strong> (Unicode) y <strong>JetOpenTableA</strong> (ANSI).</p> | 



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
