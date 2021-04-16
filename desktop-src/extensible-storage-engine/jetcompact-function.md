---
description: 'Más información acerca de: JetCompact (función)'
title: JetCompact función)
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
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716168"
---
# <a name="jetcompact-function"></a>JetCompact función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetcompact-function"></a>JetCompact función)

La función **JetCompact** realiza una copia de una base de datos existente. La copia se compacta con un estado óptimo para su uso. Los datos de los datos copiados se empaquetarán de acuerdo con las medidas elegidas para los índices en la creación de índices. De esta manera, los datos comprimidos se pueden almacenar de la forma más densa posible. Como alternativa, los datos compactos pueden reservar espacio para las inserciones de índice o el crecimiento de registros posteriores.

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

La base de datos de origen que se compactará.

*szDatabaseDest*

Nombre que se va a utilizar para la base de datos compactada.

*pfnStatus*

Función de devolución de llamada a la que se puede llamar periódicamente a través de la operación de compactación de base de datos para informar del progreso.

*pconvert*

Puntero que se usa para designar un archivo DLL de ESE alternativo que se puede usar para leer la base de datos de origen y para proporcionar parámetros opcionales para una operación **JetCompact** que está convirtiendo una base de datos de un formato de versión anterior a posterior. Esta característica se ha suspendido en Windows Server 2003.

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
<td><p>JET_bitCompactRepair</p></td>
<td><p>Se usa cuando se sabe que la base de datos de origen está dañada. Habilita un conjunto completo de nuevos comportamientos para recuperar tantos datos como sea posible de la base de datos de origen. <strong>JetCompact</strong> con este conjunto de opciones puede devolver JET_errSuccess pero no copiar todos los datos creados en la base de datos de origen. Se omitirán los datos que se encontraban en partes dañadas de la base de datos de origen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCompactStats</p></td>
<td><p>Hace que <strong>JetCompact</strong> vuelque las estadísticas de la base de datos de origen en un archivo denominado DFRGINFO.TXT. Las estadísticas incluyen el nombre de cada tabla en la base de datos de origen, el número de filas de cada tabla, el tamaño total en bytes de todas las filas de cada tabla, el tamaño total en bytes de todas las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> que eran lo suficientemente grandes como para almacenarse por separado del registro, el número de páginas hoja del índice clúster y el número de páginas Además, también se vuelcan todas las estadísticas de Resumen, incluido el tamaño de la base de datos de origen, la base de datos de destino, el tiempo necesario para la compactación de bases de datos.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Se ha proporcionado un puntero <em>pconvert</em> que no es null, pero la versión de ese que se está usando no admite la característica Convert. Esta característica se ha quitado de la versión 2003 de Windows Server de ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>La sesión que realiza la llamada se encuentra dentro de una transacción. Una sesión fuera de cualquier transacción debe llamar a <strong>JetCompact</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la base de datos de origen se copia en la base de datos de destino. La base de datos de destino está en un estado óptimo; por ejemplo, todos los índices de tabla se encuentran en un espacio de disco lógico adyacente. Cada página de índice se rellenará hasta la cantidad configurada cuando los índices se crearon originalmente en la base de datos de origen. Toda la configuración de datos y metadatos se copia con plena fidelidad, a menos que se haya especificado la opción de reparación. Si se ha especificado la opción de reparación, es posible que no se hayan copiado algunos datos de la base de datos de origen.

En caso de error, la base de datos de destino puede existir pero no es una copia completa de la base de datos de origen.

#### <a name="remarks"></a>Observaciones

La compactación de una base de datos también se usa para actualizar una base de datos de un formato de versión anterior a una versión más moderna. Un parámetro opcional es *pconvert*, que contiene una estructura que puede contener una descripción para un archivo dll de una versión anterior que se utilizará para leer el formato de la base de datos de origen. Esta característica se ha suspendido en Windows Server 2003. Después de Windows Server 2003, las nuevas versiones de ESE siempre pueden leer versiones anteriores del formato de la base de datos y, por lo tanto, esta característica no es necesaria.

La densidad deseada de datos después de una operación de compactación se especifica cuando se crean tablas e índices. La densidad debe estar comprendida entre el 20% y el 100%. Si una base de datos se lee principalmente y no se actualiza, las aplicaciones establecerán la densidad en 100% para reducir el número de operaciones de e/s durante el procesamiento de la consulta. Sin embargo, si los datos se actualizan con frecuencia con operaciones que aumentan el tamaño de los datos almacenados junto con el registro, o cuando se insertan nuevos datos con frecuencia, la aplicación elegirá una densidad inferior para que las actualizaciones encuentren con mayor frecuencia los recursos necesarios disponibles. La operación de compactar la base de datos hace que la base de datos se disponga idealmente según el relleno elegido por la aplicación.

La compactación de base de datos es una operación sin conexión. No se puede realizar mientras la base de datos está en uso. Como resultado, normalmente se hace como parte de un proceso de compilación para desarrollar una aplicación que entrega un conjunto de datos como parte de sí mismo.

La compactación de base de datos sin conexión toca cada bit de datos de una base de datos y se puede usar como un medio para comprobar la coherencia de una base de datos. Si una base de datos es sospechosa, se puede compactar. Si no se encuentra ningún error en la compactación, se sabe que la base de datos está en un estado válido para ESE.

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
<td><p>Se implementa como <strong>JetCompactW</strong> (Unicode) y <strong>JetCompactA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
