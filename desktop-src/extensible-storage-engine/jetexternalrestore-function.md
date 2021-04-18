---
description: 'Más información acerca de: JetExternalRestore (función)'
title: JetExternalRestore función)
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105708131"
---
# <a name="jetexternalrestore-function"></a>JetExternalRestore función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>JetExternalRestore función)

La función **JetExternalRestore** restaura una copia de seguridad externa que se tomó con las API de copia de seguridad externas y especifica un intervalo de números de archivo de registro que se van a reproducir durante el proceso de restauración. Esto se conoce como recuperación de hardware, que es similar a la recuperación de software, pero diferente de la que realiza la función [JetInit](./jetinit-function.md) .

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parámetros

*szCheckpointFilePath*

La ruta de acceso del archivo de punto de comprobación que se va a usar durante la recuperación si *szTargetInstanceCheckpointPath* no se especifica o si ya tiene una instancia activa o en ejecución.

*szLogPath*

La ruta de acceso o el directorio de los registros de la fase final (Deshacer) de la recuperación y, posiblemente, de los registros de puesta al día. Esta ruta de acceso puede ser la misma que la *szBackupLogPath*.

*rgrstmap*

Se trata de una matriz de estructuras [JET_RSTMAP](./jet-rstmap-structure.md) . Se trata de una asignación de nombres de archivo o rutas de acceso de base de datos antiguos y nuevos. Se usa porque las bases de datos pueden tener que recuperarse en una ubicación distinta de la ubicación desde la que se realizó la copia de seguridad. En el caso de que varias bases de datos se adjunten a un único conjunto de registros, la asignación de restauración puede especificar un subconjunto de bases de datos que se van a restaurar.

*crstfilemap*

El número de entradas en el parámetro de matriz *rgrstmap* .

*szBackupLogPath*

La ruta de acceso al directorio donde se restauran los archivos de registro. Estos son los registros que se leyeron durante la secuencia de copia de seguridad externa. Esta ruta de acceso puede ser la misma que la szLogPath.

*genLow*

El número de archivo de registro más bajo que se va a reproducir desde *szBackupLogPath*. Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto puede cambiar en versiones futuras.

*genHigh*

El número de archivo de registro más alto que se va a reproducir desde *szBackupLogPath*. Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto puede cambiar en versiones futuras.

*pfn*

Devolución de llamada de estado para informar sobre el progreso de la recuperación.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetExternalRestore</strong>, y así sucesivamente cuando <em>szTargetCheckpointPath</em> y <em>szTargetInstanceLogPath</em> no se especifican o no se especifican. Es decir, deben coincidir y estar especificados o no especificados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Esto indica que la base de datos está dañada o un archivo no reconocido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Se devuelve este error si el archivo de base de datos especificado durante la restauración no es una base de datos de la que se hizo copia de seguridad con copia de seguridad externa.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro por debajo de la que especifica <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro anterior que se especifica en <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>El <em>szTargetInstanceLogPath</em> especificado no pertenece a una instancia inicializada. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>El motor de base de datos no puede ejecutar la restauración externa o la recuperación de hardware en modo de instancia única. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, todas las bases de datos de *rgrstmap* se recuperan completamente y en un estado limpio o coherente. En este momento, la base de datos se puede volver a montar en una instancia existente.

En caso de error, el motor no pudo recuperar la base de datos. La base de datos está en un estado no válido y, para volver a intentar la recuperación de hardware, se debe restaurar toda la base de datos. Normalmente, el origen de esta situación es el disco o el registro dañado, o algún otro tipo de administración incorrecta del registro, o un conjunto de registros no continuos.

#### <a name="remarks"></a>Observaciones

Para entender cómo funciona una recuperación "fuerte", debe comprender que hay tres fases de recuperación y que la segunda fase puede tener dos partes. En la fase I, los registros son necesarios para que una base de datos de copia de seguridad sea coherente (o se puede usar un conjunto inicial de registros incrementales). En la fase II, se consume cualquier registro de puesta al día adicional que esté disponible para que la base de datos sea coherente. También hay una reproducción de los registros de puesta al día adicionales. La fase III es la fase de deshacer de la recuperación.

Fase I: se realiza la reproducción del conjunto de registros que se deben restaurar para la base de datos a un estado coherente (o un conjunto inicial de archivos de registro). Básicamente, se trata de la reproducción del conjunto de archivos de registro que no son opcionales para las bases de datos que se están restaurando. Si faltan registros de este intervalo de registros, se producirá un error en la restauración. Estos registros deben colocarse en el directorio especificado en el parámetro *szBackupLogPath* .

Fase II: opcionalmente, puede haber algunos conjuntos de archivos de registro que son los archivos de registro de puesta al día que proceden de copias de seguridad incrementales o diferenciales y de los archivos de registro de una instancia activa. En el caso de los archivos de registro de copias de seguridad incrementales o diferenciales, los archivos de registro se pueden colocar en los directorios especificados en los parámetros *szBackupLogPath* o *szTargetInstanceLogPath* , donde el primero es el directorio recomendado. Los registros que se usan para la fase de puesta al día (fase II) deben provienen de la misma serie de registros que se han producido durante la fase I y deben incrementar continuamente los números de registro sin brechas en los registros de la fase I. Para reproducir una base de datos que esté totalmente actualizada con los archivos de registro utilizados actualmente por una instancia activa, se deben especificar los parámetros *szTargetInstanceLogPath* y *szTargetInstanceCheckpointPath* . Esto se puede hacer incluso mientras otras bases de datos se adjuntan a ese conjunto de registros.

Fase III: en la fase final de la recuperación, las transacciones no confirmadas se revierten, lo que requiere la generación de nuevos archivos de registro y la actualización del archivo de punto de comprobación. Esta fase se conoce a veces como "deshacer". La ruta de acceso del archivo de punto de comprobación que se va a usar durante esta fase es la ruta de acceso análoga a la ubicación del registro de la fase III, es decir, si se usa *szLogPath* para la fase III, se usará *szCheckpointFilePath* si se usa *szTargetInstanceLogPath* para la fase III de recuperación *szTargetInstanceCheckpointPath* .

Para comprender cómo funcionan las rutas de acceso, use este diagrama de flujo:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

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
<td><p>Se implementa como <strong>JetExternalRestoreW</strong> (Unicode) y <strong>JetExternalRestoreA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
