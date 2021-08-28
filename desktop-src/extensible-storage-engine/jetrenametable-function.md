---
description: 'Más información sobre: JetRenameTable (Función)'
title: JetRenameTable (Función)
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d91f7af4896e5cb3145321de087a2803aaddd09
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985748"
---
# <a name="jetrenametable-function"></a>JetRenameTable (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetrenametable-function"></a>JetRenameTable (Función)

La **función JetRenameTable** se puede usar para cambiar el nombre de una tabla existente.

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*Dbid*

Base de datos que se va a usar para esta llamada.

*szName*

Nombre actual de la tabla cuyo nombre se va a cambiar.

*szNameNew*

Nuevo nombre de la tabla cuyo nombre se va a cambiar.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>La base de datos especificada no era válida.</p><p>Este error solo se devuelve en Windows 2000 cuando se intenta realizar una operación de cambio de nombre de tabla en la base de datos temporal. JET_errInvalidDatabaseId se devuelve para este caso en versiones posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>El identificador de base de datos especificado no era válido.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno de los nombres de objeto especificados no era válido. Todos los nombres de objeto deben cumplir el mismo conjunto de reglas. Estas reglas son:</p><ul><li><p>Los nombres de objeto deben estar compuestos de caracteres ASCII.</p></li><li><p>Los nombres de objeto deben tener al menos un carácter de longitud.</p></li><li><p>Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</p></li><li><p>Es posible que los nombres de objeto no comiencen por un espacio.</p></li><li><p>Los nombres de objeto no pueden contener caracteres de control ASCII (0x00 a 0x1F).</p></li><li><p>Los nombres de objeto no pueden contener un signo de exclamación (!), punto (.), corchete izquierdo ([) o corchete derecho (]): una vez validado, solo se usará la parte de la cadena hasta el primer espacio (si lo hubiera) para el nombre del objeto. Esto significa de hecho que los nombres de objeto tampoco pueden contener un espacio.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetRenameTable</strong> cuando:</p><ul><li><p><em>szName</em> es NULL.</p></li><li><p><em>szNameNew</em> es NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Esta tabla especificada no existe para esta base de datos.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>No se puede realizar una actualización dentro del ámbito de una transacción de solo lectura. Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 



Si se ejecuta correctamente, el nombre de la tabla especificada en la base de datos especificada se cambia permanentemente al nuevo nombre.

En caso de error, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetRenameTableW</strong> (Unicode) y <strong>JetRenameTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
