---
description: 'Más información acerca de: miembros de InstanceParameters'
title: Miembros de InstanceParameters
TOCTitle: InstanceParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_members(v=EXCHG.10)
ms:contentKeyID: 55103286
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8d52035b7473c17f9278a0343d12d957b2970349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568326"
---
# <a name="instanceparameters-members"></a>Miembros de InstanceParameters

Incluir miembros protegidos  
Incluir miembros heredados  

Esta clase proporciona propiedades para establecer y obtener parámetros del sistema en una instancia de ESENT. Esta clase proporciona propiedades estáticas para establecer y obtener parámetros del sistema ESENT por instancia.

El tipo [InstanceParameters](./instanceparameters-class.md) expone los siguientes miembros.

## <a name="constructors"></a>Constructores

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350965(v=exchg.10).md">InstanceParameters</a></td>
<td>Inicializa una nueva instancia de la clase InstanceParameters.</td>
</tr>
</tbody>
</table>


Superior

## <a name="properties"></a>Propiedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></td>
<td>Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta en la que la recuperación tras bloqueo o una operación de restauración pueden encontrar las bases de datos a las que se hace referencia en el registro de transacciones de la carpeta especificada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">BaseName</a></td>
<td>Obtiene o establece el prefijo de tres letras utilizado para muchos de los archivos utilizados por el motor de base de datos. Por ejemplo, el archivo de punto de comprobación se denomina EDB. CHK de forma predeterminada porque EDB es el nombre base predeterminado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>Obtiene o establece un valor que indica el número de recursos de árbol B + almacenados en memoria caché por la instancia después de que la aplicación haya cerrado las tablas que representan. Los valores grandes de este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas. Esto resulta útil para las aplicaciones que tienen un esquema con un gran número de tablas. Compatible con Windows Vista y up. Se omite en Windows XP y Windows Server 2003.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>Obtiene o establece la propiedad por instancia para las prioridades de caché relativas (valor predeterminado = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Obtiene o establece el umbral en bytes para el número de archivos de registro de transacciones que se deben reproducir después de un bloqueo. Si el registro circular está habilitado mediante CircularLog, este parámetro también controlará la cantidad aproximada de archivos de registro de transacciones que se conservarán en el disco.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>Obtiene o establece un valor que indica si el registro circular está activado. Cuando el registro circular está desactivado, todos los archivos de registro de transacciones que se generan se conservan en el disco hasta que ya no son necesarios porque se ha realizado una copia de seguridad completa de la base de datos. Cuando el registro circular está activado, solo se conservan en el disco los archivos de registro de transacciones que son más jóvenes que el punto de control actual. La ventaja de este modo es que las copias de seguridad no son necesarias para retirar los archivos de registro de transacciones antiguos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>Obtiene o establece un valor que indica si se produce un error en JetInit cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en un disco con un tamaño diferente del configurado. Normalmente, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> recuperará correctamente las bases de datos, pero producirá un error con <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> para indicar que el tamaño del archivo de registro está mal configurado. Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará silenciosamente todos los archivos de registro antiguos, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño del archivo de registro configurado. Este parámetro es útil cuando la aplicación desea cambiar de forma transparente el tamaño del archivo de registro de transacciones todavía funciona de forma transparente en los escenarios de actualización y restauración.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>Obtiene o establece un valor que indica si ESENT creará silenciosamente carpetas que faltan en sus rutas de acceso del sistema de archivos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>Obtiene o establece el número de páginas que se agregan a un archivo de base de datos cada vez que necesita crecer para alojar más datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Obtiene o establece el intervalo máximo para permitir que finalice el examen de la base de datos, en segundos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Obtiene o establece el intervalo mínimo para repetir el análisis de base de datos, en segundos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>Obtiene o establece la limitación del análisis de base de datos, en milisegundos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Obtiene o establece un valor que indica si el mantenimiento de la base de datos se debe ejecutar durante la recuperación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>Obtiene o establece un valor que indica si está habilitada la serialización del mantenimiento de la base de datos para las bases de datos que comparten el mismo disco.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>Obtiene o establece un valor que indica si <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> comprobará si hay índices compilados con una versión anterior de la biblioteca NLS en el sistema operativo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>Obtiene o establece un valor que indica si está habilitada la desfragmentación con conexión.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>Obtiene o establece una cadena específica de la aplicación que se agregará a los mensajes del registro de eventos emitidos por el motor de base de datos. Esto permite la correlación sencilla de mensajes de registro de eventos con la aplicación de origen. De forma predeterminada, se usará el nombre del archivo ejecutable de la aplicación host.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Obtiene o establece el nombre del registro de eventos que usa el motor de base de datos para sus mensajes de registro de eventos. De forma predeterminada, todos los mensajes del registro de eventos Irán al registro de eventos de la aplicación. Si se configura el nombre de la clave del registro para otro registro de eventos, los mensajes del registro de eventos Irán en su lugar.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffers</a></td>
<td>Obtiene o establece la cantidad de memoria que se usa para almacenar en memoria caché las entradas del registro antes de que se escriban en el archivo de registro de transacciones. La unidad para este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones. El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro suponer ese tamaño para la unidad. Este parámetro afecta al rendimiento. Cuando el motor de base de datos está sometido a una carga de actualización pesada, este búfer puede llenarse con mucha rapidez. Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga elevada. Se sabe que el valor predeterminado es demasiado pequeño para este caso. No establezca este parámetro en un número de búferes mayor (en bytes) de la mitad del tamaño de un archivo de registro de transacciones.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá los registros de transacciones de la instancia.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>Obtiene o establece el tamaño de los archivos de registro de transacciones. Este parámetro debe establecerse en unidades de 1024 bytes (por ejemplo, un valor de 2048 proporcionará 2 MB de archivo de registro).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>Obtiene o establece el número de recursos de cursor reservados para esta instancia. Un recurso cursor se corresponde directamente con un JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Obtiene o establece el número de recursos de árbol B + reservados para esta instancia.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Obtiene o establece el número de recursos de sesión reservados para esta instancia. Un recurso de sesión se corresponde directamente con un JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>Obtiene o establece el número de recursos de tabla temporal que va a usar una instancia de. Esta configuración afectará al número de tablas temporales que se pueden usar al mismo tiempo. Si este parámetro del sistema se establece en cero, no se creará ninguna base de datos temporal y se producirá un error en cualquier actividad que requiera el uso de la base de datos temporal. Esta configuración puede ser útil para evitar la e/s necesaria para crear la base de datos temporal si se sabe que no se va a usar.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>Obtiene o establece el porcentaje del almacén de versiones que la transacción más antigua puede usar antes de <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (valor predeterminado = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Obtiene o establece el número máximo de páginas del almacén de versiones reservadas para esta instancia.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>Obtiene o establece un valor que indica si se suprimen los mensajes de registro de eventos informativos que normalmente generarían el motor de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>Obtiene o establece un valor que indica si solo se permite abrir una base de datos mediante JetOpenDatabase por una sesión determinada al mismo tiempo. La base de datos temporal se excluye de esta restricción.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>Obtiene o establece el tamaño inicial de la base de datos temporal. El tamaño está en páginas de base de datos. Un tamaño de cero indica que se debe usar el tamaño predeterminado de una base de datos normal. A menudo, es deseable que las aplicaciones pequeñas configuren la base de datos temporal para que sea lo más pequeña posible. Si se establece este parámetro en <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> , se logrará la base de datos temporal más pequeña posible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>Obtiene o establece el número preferido de páginas del almacén de versiones reservadas para esta instancia. Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se use para tareas en segundo plano opcionales, como la recuperación del espacio eliminado en la base de datos, se sacrifica en su lugar para conservar el espacio para la información transaccional.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>Obtiene o establece el número máximo de operaciones de e/s enviadas para un propósito determinado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Recuperación</a></td>
<td>Obtiene o establece un valor que indica si la recuperación de bloqueos está activada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá el archivo de punto de comprobación de la instancia.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá la base de datos temporal de la instancia.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>Obtiene o establece el número de elementos de trabajo de limpieza en segundo plano que se pueden poner en cola en el grupo de subprocesos del motor de base de datos al mismo tiempo.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>Obtiene o establece el número de registros que esent aplazará los vaciados de la base de datos. Se puede usar para aumentar la capacidad de recuperación de la base de datos si los errores provocan la pérdida de los archivos de registro. Compatible con Windows 7 y up. Se omite en Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008.</td>
</tr>
</tbody>
</table>


Superior

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350967(v=exchg.10).md">ToString</a></td>
<td>Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn350942(v=exchg.10).md">InstanceParameters</a>actual. (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
