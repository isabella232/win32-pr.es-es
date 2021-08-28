---
description: 'Más información sobre: JetExternalRestore (Función)'
title: JetExternalRestore (Función)
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
ms.openlocfilehash: 480a3411152f1388bee0115ecbcffc88f6ded09b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984858"
---
# <a name="jetexternalrestore-function"></a>JetExternalRestore (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetexternalrestore-function"></a>JetExternalRestore (Función)

La **función JetExternalRestore** restaura una copia de seguridad externa realizada con las API de copia de seguridad externas y especifica un intervalo de números de archivo de registro que se reproducirán durante el proceso de restauración. Esto se conoce como recuperación de disco duro, que es similar a la recuperación de software, pero diferente a la realizada por la [función JetInit.](./jetinit-function.md)

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

Ruta de acceso del archivo de punto de control que se usará durante la recuperación si no se especifica *szTargetInstanceCheckpointPath* o si ya tiene una instancia activa o en ejecución.

*szLogPath*

Ruta de acceso o directorio para los registros de la fase final (deshacer) de la recuperación y, posiblemente, para los registros de reversión. Esta ruta de acceso puede ser la misma que *szBackupLogPath*.

*rgrstmap*

Se trata de una matriz [de JET_RSTMAP](./jet-rstmap-structure.md) estructuras. Se trata de un mapa de rutas de acceso o nombres de archivo de base de datos antiguos y nuevos. Esto se usa porque es posible que las bases de datos deban recuperarse en una ubicación que no sea la ubicación desde la que se ha hecho una copia de seguridad. En el caso de que varias bases de datos estén asociadas a un único conjunto de registro, el mapa de restauración puede especificar un subconjunto de bases de datos para restaurar.

*crstfilemap*

Número de entradas del parámetro *de matriz rgrstmap.*

*szBackupLogPath*

Ruta de acceso al directorio donde se restauran los archivos de registro. Estos son los registros que se leyeron durante la secuencia de copia de seguridad externa. Esta ruta de acceso puede ser la misma que szLogPath.

*genLow*

Número de archivo de registro más bajo que se va a reproducir desde *szBackupLogPath.* Se debe conservar la fidelidad total de un long sin signo, pero en las versiones actuales del motor este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto puede cambiar en versiones futuras.

*genHigh*

Número de archivo de registro más alto que se va a reproducir desde *szBackupLogPath.* Se debe conservar la fidelidad total de un long sin signo, pero en las versiones actuales del motor este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto puede cambiar en versiones futuras.

*pfn*

Devolución de llamada de estado, para informar del progreso de la recuperación.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir <strong>para JetExternalRestore,</strong>y así sucesivamente cuando <em>szTargetCheckpointPath</em> y <em>szTargetInstanceLogPath</em> no se especifican o no se especifican ambos. Es decir, deben coincidir y deben especificarse o no especificarse ambos.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Esto indica que la base de datos está dañada o un archivo no reconocido.</p> | 
| <p>JET_errFileNotFound</p> | <p>Error en la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</p> | 
| <p>JET_errInvalidPath</p> | <p>Error en la operación porque no se encontró la ruta de acceso especificada.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Este error se devuelve si el archivo de base de datos especificado durante la restauración no es una base de datos de la que se ha hecho una copia de seguridad externa.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registros inferior a la especificada por <em>genLow</em> o <em>pLogInfo.ulGenLow</em>.</p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registros anterior a la especificada en <em>genHigh</em> o <em>pLogInfo.ulGenHigh</em>.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>El <em>szTargetInstanceLogPath</em> especificado no pertenece a una instancia inicializada. Este error solo se devolverá en Windows XP y versiones posteriores.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>El motor de base de datos no puede ejecutar la restauración externa ni la recuperación en modo de instancia única. Este error solo se devolverá en Windows XP y versiones posteriores.</p> | 



Si se ejecuta correctamente, todas las bases de datos de *rgrstmap* se recuperan completamente y en un estado limpio o coherente. En este momento, la base de datos se puede volver a montar en una instancia existente.

En caso de error, el motor no pudo recuperar la base de datos. La base de datos está en un estado no válido y, para reintentar la recuperación, toda la base de datos debe restaurarse de nuevo. Normalmente, el origen de este tipo de situación son daños en el disco o el registro, algún otro tipo de administración errónea del registro o un conjunto de registros no continuo.

#### <a name="remarks"></a>Observaciones

Para entender cómo funciona una recuperación "dura", debe comprender que hay tres fases de recuperación y que la segunda fase puede tener dos partes. En la fase I, los registros son necesarios para mantener la coherencia de una base de datos de la que se ha hecho una copia de seguridad (o se puede usar un conjunto inicial de registros incrementales). En la fase II, se consumen los registros de reversión adicionales que están disponibles para que la base de datos sea coherente. También hay una reproducción de los registros de reversión adicionales. Fase III es la fase de deshacer de la recuperación.

Fase I: se realiza la reproducción del conjunto de registros que se debe restaurar para que la base de datos tenga un estado coherente (o un conjunto inicial de archivos de registro). Básicamente, se trata de la reproducción del conjunto de archivos de registro que no son opcionales para las bases de datos que se restauran. Si faltan registros de este intervalo de registros, se producirá un error en la restauración. Estos registros deben colocarse en el directorio especificado en el *parámetro szBackupLogPath.*

Fase II: Opcionalmente, puede haber algunos conjuntos de archivos de registro que son archivos de registro de reversión que proceden de copias de seguridad incrementales o diferenciales y de los archivos de registro de una instancia activa. En el caso de los archivos de registro de copias de seguridad incrementales o diferenciales, los archivos de registro se pueden colocar en los directorios especificados en los parámetros *szBackupLogPath* o *szTargetInstanceLogPath,* siendo el primero el directorio recomendado. Los registros usados para la fase de implementación (fase II) deben proceden de la misma serie de registros que se reproducen durante la fase I y deben incrementar continuamente los números de registro sin espacios en los registros de la fase I. Para reproducir una base de datos para que esté totalmente actualizada con los archivos de registro que usa actualmente una instancia activa, se deben especificar los parámetros *szTargetInstanceLogPath* y *szTargetInstanceCheckpointPath.* Esto se puede hacer incluso mientras otras bases de datos están asociadas a ese conjunto de registros.

Fase III: en la fase final de la recuperación, se revierten las transacciones no confirmadas, lo que requiere generar nuevos archivos de registro y actualizar el archivo de punto de comprobación. Esta fase se conoce a veces como "deshacer". La ruta de acceso del archivo de punto de comprobación que se usará durante esta fase es la ruta de acceso análoga a la ubicación del registro de fase III, es decir, si se usa *szLogPath* para la fase III, se usará *szCheckpointFilePath,* si se usa *szTargetInstanceLogPath* para la fase III de recuperación *szTargetInstanceCheckpointPath.*

Para comprender cómo funcionan las rutas de acceso, use este gráfico de flujo:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetExternalRestoreW</strong> (Unicode) y <strong>JetExternalRestoreA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
