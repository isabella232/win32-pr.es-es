---
description: 'Más información acerca de: propiedades de InstanceParameters'
title: Propiedades de InstanceParameters
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0ac2b8aa959b8fa07f06e2de86dcfc173bab15ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559286"
---
# <a name="instanceparameters-properties"></a><span data-ttu-id="1ad69-103">Propiedades de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="1ad69-103">InstanceParameters properties</span></span>

<span data-ttu-id="1ad69-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="1ad69-104">Include protected members</span></span>  
<span data-ttu-id="1ad69-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="1ad69-105">Include inherited members</span></span>  

<span data-ttu-id="1ad69-106">El tipo [InstanceParameters](./instanceparameters-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="1ad69-106">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="1ad69-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ad69-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1ad69-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ad69-108">Name</span></span></th>
<th><span data-ttu-id="1ad69-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ad69-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="1ad69-112">Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta en la que la recuperación tras bloqueo o una operación de restauración pueden encontrar las bases de datos a las que se hace referencia en el registro de transacciones de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="1ad69-112">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="1ad69-115">Obtiene o establece el prefijo de tres letras utilizado para muchos de los archivos utilizados por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-115">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="1ad69-116">Por ejemplo, el archivo de punto de comprobación se denomina EDB. CHK de forma predeterminada porque EDB es el nombre base predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ad69-116">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="1ad69-119">Obtiene o establece un valor que indica el número de recursos de árbol B + almacenados en memoria caché por la instancia después de que la aplicación haya cerrado las tablas que representan.</span><span class="sxs-lookup"><span data-stu-id="1ad69-119">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="1ad69-120">Los valores grandes de este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="1ad69-120">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="1ad69-121">Esto resulta útil para las aplicaciones que tienen un esquema con un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="1ad69-121">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="1ad69-122">Compatible con Windows Vista y up.</span><span class="sxs-lookup"><span data-stu-id="1ad69-122">Supported on Windows Vista and up.</span></span> <span data-ttu-id="1ad69-123">Se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1ad69-123">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="1ad69-126">Obtiene o establece la propiedad por instancia para las prioridades de caché relativas (valor predeterminado = 100).</span><span class="sxs-lookup"><span data-stu-id="1ad69-126">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="1ad69-129">Obtiene o establece el umbral en bytes para el número de archivos de registro de transacciones que se deben reproducir después de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="1ad69-129">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="1ad69-130">Si el registro circular está habilitado mediante CircularLog, este parámetro también controlará la cantidad aproximada de archivos de registro de transacciones que se conservarán en el disco.</span><span class="sxs-lookup"><span data-stu-id="1ad69-130">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="1ad69-133">Obtiene o establece un valor que indica si el registro circular está activado.</span><span class="sxs-lookup"><span data-stu-id="1ad69-133">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="1ad69-134">Cuando el registro circular está desactivado, todos los archivos de registro de transacciones que se generan se conservan en el disco hasta que ya no son necesarios porque se ha realizado una copia de seguridad completa de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-134">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="1ad69-135">Cuando el registro circular está activado, solo se conservan en el disco los archivos de registro de transacciones que son más jóvenes que el punto de control actual.</span><span class="sxs-lookup"><span data-stu-id="1ad69-135">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="1ad69-136">La ventaja de este modo es que las copias de seguridad no son necesarias para retirar los archivos de registro de transacciones antiguos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-136">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="1ad69-139">Obtiene o establece un valor que indica si se produce un error en JetInit cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en un disco con un tamaño diferente del configurado.</span><span class="sxs-lookup"><span data-stu-id="1ad69-139">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="1ad69-140">Normalmente, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> recuperará correctamente las bases de datos, pero producirá un error con <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> para indicar que el tamaño del archivo de registro está mal configurado.</span><span class="sxs-lookup"><span data-stu-id="1ad69-140">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="1ad69-141">Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará silenciosamente todos los archivos de registro antiguos, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño del archivo de registro configurado.</span><span class="sxs-lookup"><span data-stu-id="1ad69-141">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="1ad69-142">Este parámetro es útil cuando la aplicación desea cambiar de forma transparente el tamaño del archivo de registro de transacciones todavía funciona de forma transparente en los escenarios de actualización y restauración.</span><span class="sxs-lookup"><span data-stu-id="1ad69-142">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="1ad69-145">Obtiene o establece un valor que indica si ESENT creará silenciosamente carpetas que faltan en sus rutas de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-145">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="1ad69-148">Obtiene o establece el número de páginas que se agregan a un archivo de base de datos cada vez que necesita crecer para alojar más datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-148">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="1ad69-151">Obtiene o establece el intervalo máximo para permitir que finalice el examen de la base de datos, en segundos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-151">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="1ad69-154">Obtiene o establece el intervalo mínimo para repetir el análisis de base de datos, en segundos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-154">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="1ad69-157">Obtiene o establece la limitación del análisis de base de datos, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-157">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="1ad69-160">Obtiene o establece un valor que indica si el mantenimiento de la base de datos se debe ejecutar durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="1ad69-160">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="1ad69-163">Obtiene o establece un valor que indica si está habilitada la serialización del mantenimiento de la base de datos para las bases de datos que comparten el mismo disco.</span><span class="sxs-lookup"><span data-stu-id="1ad69-163">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="1ad69-166">Obtiene o establece un valor que indica si <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> comprobará si hay índices compilados con una versión anterior de la biblioteca NLS en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1ad69-166">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="1ad69-169">Obtiene o establece un valor que indica si está habilitada la desfragmentación con conexión.</span><span class="sxs-lookup"><span data-stu-id="1ad69-169">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="1ad69-172">Obtiene o establece una cadena específica de la aplicación que se agregará a los mensajes del registro de eventos emitidos por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-172">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="1ad69-173">Esto permite la correlación sencilla de mensajes de registro de eventos con la aplicación de origen.</span><span class="sxs-lookup"><span data-stu-id="1ad69-173">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="1ad69-174">De forma predeterminada, se usará el nombre del archivo ejecutable de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="1ad69-174">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="1ad69-177">Obtiene o establece el nombre del registro de eventos que usa el motor de base de datos para sus mensajes de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-177">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="1ad69-178">De forma predeterminada, todos los mensajes del registro de eventos Irán al registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1ad69-178">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="1ad69-179">Si se configura el nombre de la clave del registro para otro registro de eventos, los mensajes del registro de eventos Irán en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1ad69-179">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="1ad69-182">Obtiene o establece la cantidad de memoria que se usa para almacenar en memoria caché las entradas del registro antes de que se escriban en el archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="1ad69-182">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="1ad69-183">La unidad para este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="1ad69-183">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="1ad69-184">El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro suponer ese tamaño para la unidad.</span><span class="sxs-lookup"><span data-stu-id="1ad69-184">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="1ad69-185">Este parámetro afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1ad69-185">This parameter has an impact on performance.</span></span> <span data-ttu-id="1ad69-186">Cuando el motor de base de datos está sometido a una carga de actualización pesada, este búfer puede llenarse con mucha rapidez.</span><span class="sxs-lookup"><span data-stu-id="1ad69-186">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="1ad69-187">Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga elevada.</span><span class="sxs-lookup"><span data-stu-id="1ad69-187">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="1ad69-188">Se sabe que el valor predeterminado es demasiado pequeño para este caso.</span><span class="sxs-lookup"><span data-stu-id="1ad69-188">The default is known to be too small for this case.</span></span> <span data-ttu-id="1ad69-189">No establezca este parámetro en un número de búferes mayor (en bytes) de la mitad del tamaño de un archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="1ad69-189">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="1ad69-192">Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá los registros de transacciones de la instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-192">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="1ad69-195">Obtiene o establece el tamaño de los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="1ad69-195">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="1ad69-196">Este parámetro debe establecerse en unidades de 1024 bytes (por ejemplo, un valor de 2048 proporcionará 2 MB de archivo de registro).</span><span class="sxs-lookup"><span data-stu-id="1ad69-196">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="1ad69-199">Obtiene o establece el número de recursos de cursor reservados para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-199">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="1ad69-200">Un recurso cursor se corresponde directamente con un JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="1ad69-200">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="1ad69-203">Obtiene o establece el número de recursos de árbol B + reservados para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-203">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="1ad69-206">Obtiene o establece el número de recursos de sesión reservados para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-206">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="1ad69-207">Un recurso de sesión se corresponde directamente con un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="1ad69-207">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="1ad69-210">Obtiene o establece el número de recursos de tabla temporal que va a usar una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1ad69-210">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="1ad69-211">Esta configuración afectará al número de tablas temporales que se pueden usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1ad69-211">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="1ad69-212">Si este parámetro del sistema se establece en cero, no se creará ninguna base de datos temporal y se producirá un error en cualquier actividad que requiera el uso de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="1ad69-212">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="1ad69-213">Esta configuración puede ser útil para evitar la e/s necesaria para crear la base de datos temporal si se sabe que no se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1ad69-213">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="1ad69-216">Obtiene o establece el porcentaje del almacén de versiones que la transacción más antigua puede usar antes de <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (valor predeterminado = 100).</span><span class="sxs-lookup"><span data-stu-id="1ad69-216">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="1ad69-219">Obtiene o establece el número máximo de páginas del almacén de versiones reservadas para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-219">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="1ad69-222">Obtiene o establece un valor que indica si se suprimen los mensajes de registro de eventos informativos que normalmente generarían el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-222">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="1ad69-225">Obtiene o establece un valor que indica si solo se permite abrir una base de datos mediante JetOpenDatabase por una sesión determinada al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1ad69-225">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="1ad69-226">La base de datos temporal se excluye de esta restricción.</span><span class="sxs-lookup"><span data-stu-id="1ad69-226">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="1ad69-229">Obtiene o establece el tamaño inicial de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="1ad69-229">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="1ad69-230">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-230">The size is in database pages.</span></span> <span data-ttu-id="1ad69-231">Un tamaño de cero indica que se debe usar el tamaño predeterminado de una base de datos normal.</span><span class="sxs-lookup"><span data-stu-id="1ad69-231">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="1ad69-232">A menudo, es deseable que las aplicaciones pequeñas configuren la base de datos temporal para que sea lo más pequeña posible.</span><span class="sxs-lookup"><span data-stu-id="1ad69-232">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="1ad69-233">Si se establece este parámetro en <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> , se logrará la base de datos temporal más pequeña posible.</span><span class="sxs-lookup"><span data-stu-id="1ad69-233">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="1ad69-236">Obtiene o establece el número preferido de páginas del almacén de versiones reservadas para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-236">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="1ad69-237">Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se use para tareas en segundo plano opcionales, como la recuperación del espacio eliminado en la base de datos, se sacrifica en su lugar para conservar el espacio para la información transaccional.</span><span class="sxs-lookup"><span data-stu-id="1ad69-237">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="1ad69-240">Obtiene o establece el número máximo de operaciones de e/s enviadas para un propósito determinado.</span><span class="sxs-lookup"><span data-stu-id="1ad69-240">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-242"><a href="dn350981(v=exchg.10).md">Recuperación</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-242"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="1ad69-243">Obtiene o establece un valor que indica si la recuperación de bloqueos está activada.</span><span class="sxs-lookup"><span data-stu-id="1ad69-243">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="1ad69-246">Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá el archivo de punto de comprobación de la instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-246">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="1ad69-249">Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá la base de datos temporal de la instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad69-249">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="1ad69-252">Obtiene o establece el número de elementos de trabajo de limpieza en segundo plano que se pueden poner en cola en el grupo de subprocesos del motor de base de datos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1ad69-252">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1ad69-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span><span class="sxs-lookup"><span data-stu-id="1ad69-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="1ad69-255">Obtiene o establece el número de registros que esent aplazará los vaciados de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ad69-255">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="1ad69-256">Se puede usar para aumentar la capacidad de recuperación de la base de datos si los errores provocan la pérdida de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="1ad69-256">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="1ad69-257">Compatible con Windows 7 y up.</span><span class="sxs-lookup"><span data-stu-id="1ad69-257">Supported on Windows 7 and up.</span></span> <span data-ttu-id="1ad69-258">Se omite en Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1ad69-258">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ad69-259">Superior</span><span class="sxs-lookup"><span data-stu-id="1ad69-259">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1ad69-260">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ad69-260">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ad69-261">Referencia</span><span class="sxs-lookup"><span data-stu-id="1ad69-261">Reference</span></span>

[<span data-ttu-id="1ad69-262">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="1ad69-262">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="1ad69-263">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ad69-263">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
