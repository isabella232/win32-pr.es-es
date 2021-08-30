---
description: 'Más información sobre: JetCompact (Función)'
title: JetCompact (Función)
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea0baef0e01b9fc6dbbd3a553eb28424f02fe45b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987478"
---
# <a name="jetcompact-function"></a>JetCompact (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcompact-function"></a>JetCompact (Función)

La **función JetCompact** realiza una copia de una base de datos existente. La copia se compacta a un estado óptimo para su uso. Los datos de los datos copiados se empaquetarán según las medidas elegidas para los índices en la creación del índice. De esta manera, los datos compactados se pueden almacenar lo más densamente posible. Como alternativa, los datos compactados pueden reservar espacio para el posterior crecimiento de registros o inserciones de índices.

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*szDatabaseSrc*

Base de datos de origen que se compactará.

*szDatabaseDest*

Nombre que se usará para la base de datos compactada.

*pfnStatus*

Función de devolución de llamada a la que se puede llamar periódicamente a través de la operación compacta de base de datos para informar del progreso.

*pconvert*

Puntero que se usa para designar un archivo DLL ese alternativo que se puede usar para leer la base de datos de origen y para proporcionar parámetros opcionales para una operación **JetCompact** que convierte una base de datos de un formato anterior a un formato de versión posterior. Esta característica se descontinuó en Windows Server 2003.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCompactRepair</p> | <p>Se usa cuando se sabe que la base de datos de origen está dañada. Permite un conjunto completo de comportamientos nuevos diseñados para recuperar tantos datos como sea posible de la base de datos de origen. <strong>JetCompact</strong> con este conjunto de opciones puede devolver JET_errSuccess pero no copiar todos los datos creados en la base de datos de origen. Se omitirán los datos que se encontraban en partes dañadas de la base de datos de origen.</p> | 
| <p>JET_bitCompactStats</p> | <p>Hace <strong>que JetCompact</strong> vuelque las estadísticas de la base de datos de origen en un archivo denominado DFRGINFO.TXT. Las estadísticas incluyen el nombre de cada tabla de la base de datos de origen, el número de filas de cada tabla, el tamaño total en bytes de todas las filas de cada tabla, el tamaño total en bytes de todas las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> que eran lo suficientemente grandes como para almacenarse independientes del registro, el número de páginas hoja de índice agrupado y el número de páginas hoja de valor largo. Además, también se vuelca el tamaño de la base de datos de origen, la base de datos de destino, el tiempo necesario para la compactación de la base de datos y el espacio temporal de la base de datos.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Se ha proporcionado un puntero <em>pconvert</em> que no es NULL, pero la versión de ESE que se usa no admite la característica de conversión. Esta característica se quitó en la versión Windows Server 2003 de ESE.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInTransaction</p> | <p>La sesión de llamada está dentro de una transacción. Una sesión fuera de cualquier transacción debe llamar a <strong>JetCompact.</strong></p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, la base de datos de origen se copia en la base de datos de destino. La base de datos de destino está en un estado óptimo, por ejemplo, todos los índices de tabla se encuentran en un espacio en disco lógico adyacente. Cada página de índice se agrega a la cantidad configurada cuando los índices se crearon originalmente en la base de datos de origen. Todos los datos y la configuración de metadatos se copian con total fidelidad, a menos que se haya especificado la opción de reparación. Si se especificó la opción de reparación, es posible que algunos datos de la base de datos de origen no se hayan copiado.

En caso de error, la base de datos de destino puede existir, pero no es una copia completa de la base de datos de origen.

#### <a name="remarks"></a>Observaciones

La compactación de una base de datos también se usa para actualizar una base de datos de un formato de versión anterior a una versión más moderna. Un parámetro opcional es *pconvert*, que contiene una estructura que puede contener una descripción de un archivo DLL de versión anterior que se usará para leer el formato de la base de datos de origen. Esta característica se descontinuó en Windows Server 2003. Después de Windows Server 2003, las nuevas versiones de ESE siempre pueden leer versiones anteriores del formato de base de datos y, por tanto, esta característica no es necesaria.

La densidad deseada de los datos después de una operación compacta se especifica cuando se crean tablas e índices. La densidad debe estar entre el 20 % y el 100 %. Si una base de datos se lee principalmente y no se actualiza, las aplicaciones establecerán la densidad en el 100 % para reducir el número de operaciones de E/S durante el procesamiento de consultas. Sin embargo, si los datos se actualizan con frecuencia con operaciones que aumentan el tamaño de los datos almacenados junto con el registro, o si se insertan datos nuevos con frecuencia, la aplicación elegirá una densidad inferior para que las actualizaciones encuentren más a menudo los recursos necesarios disponibles. La operación de compactación de la base de datos hace que la base de datos se pueda colocar idealmente según el relleno elegido por la aplicación.

La compactación de la base de datos es una operación sin conexión. No se puede realizar mientras la base de datos está en uso. Como resultado, normalmente se realiza como parte de un proceso de compilación de desarrollo de una aplicación que entrega un conjunto de datos como parte de sí mismo.

La compactación de base de datos sin conexión toca cada bit de datos de una base de datos y se puede usar como medio de comprobar la coherencia de una base de datos. Si una base de datos es sospechosa, se puede compactar. Si no se encuentra ningún error de compactación, se sabe que la base de datos está en un estado válido para ESE.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetCompactW</strong> (Unicode) y <strong>JetCompactA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
