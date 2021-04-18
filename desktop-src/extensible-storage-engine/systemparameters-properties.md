---
description: 'Más información acerca de: propiedades de SystemParameters'
title: Propiedades de SystemParameters
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571735"
---
# <a name="systemparameters-properties"></a><span data-ttu-id="380f4-103">Propiedades de SystemParameters</span><span class="sxs-lookup"><span data-stu-id="380f4-103">SystemParameters properties</span></span>

<span data-ttu-id="380f4-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="380f4-104">Include protected members</span></span>  
<span data-ttu-id="380f4-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="380f4-105">Include inherited members</span></span>  

<span data-ttu-id="380f4-106">El tipo [SystemParameters](./systemparameters-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="380f4-106">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="380f4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="380f4-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="380f4-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="380f4-108">Name</span></span></th>
<th><span data-ttu-id="380f4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="380f4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span><span class="sxs-lookup"><span data-stu-id="380f4-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="380f4-113">Obtiene el tamaño máximo de un marcador.</span><span class="sxs-lookup"><span data-stu-id="380f4-113">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="380f4-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="380f4-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="380f4-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="380f4-118">Obtiene o establece el tamaño de la memoria caché de la base de datos en páginas.</span><span class="sxs-lookup"><span data-stu-id="380f4-118">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="380f4-119">De forma predeterminada, la memoria caché de base de datos ajustará automáticamente su tamaño y, si se establece esta propiedad en un valor distinto de cero, la memoria caché se ajustará al tamaño de destino.</span><span class="sxs-lookup"><span data-stu-id="380f4-119">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span><span class="sxs-lookup"><span data-stu-id="380f4-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="380f4-123">Obtiene o establece el tamaño máximo de la memoria caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-123">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="380f4-124">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-124">The size is in database pages.</span></span> <span data-ttu-id="380f4-125">Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a JetInit.</span><span class="sxs-lookup"><span data-stu-id="380f4-125">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span><span class="sxs-lookup"><span data-stu-id="380f4-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="380f4-129">Obtiene o establece el tamaño mínimo de la memoria caché de páginas de base de datos, en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-129">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="380f4-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="380f4-133">Obtiene el número máximo de componentes en una clave de ordenación o de índice.</span><span class="sxs-lookup"><span data-stu-id="380f4-133">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-136"><a href="dn351218(v=exchg.10).md">Configuración</a></span><span class="sxs-lookup"><span data-stu-id="380f4-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="380f4-137">Obtiene o establece un valor que especifica los valores predeterminados para todo el conjunto de parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="380f4-137">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="380f4-138">Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración.</span><span class="sxs-lookup"><span data-stu-id="380f4-138">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="380f4-139">Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="380f4-139">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="380f4-140">Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="380f4-140">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="380f4-141">Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.</span><span class="sxs-lookup"><span data-stu-id="380f4-141">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="380f4-142">Compatible con Windows Vista y up.</span><span class="sxs-lookup"><span data-stu-id="380f4-142">Supported on Windows Vista and up.</span></span> <span data-ttu-id="380f4-143">Se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="380f4-143">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span><span class="sxs-lookup"><span data-stu-id="380f4-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="380f4-147">Obtiene o establece el tamaño de las páginas de base de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="380f4-147">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="380f4-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="380f4-151">Obtiene o establece un valor que indica si el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="380f4-151">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="380f4-152">Este parámetro se usa junto con la <a href="dn351218(v=exchg.10).md">configuración</a> para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada.</span><span class="sxs-lookup"><span data-stu-id="380f4-152">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="380f4-153">Compatible con Windows Vista y up.</span><span class="sxs-lookup"><span data-stu-id="380f4-153">Supported on Windows Vista and up.</span></span> <span data-ttu-id="380f4-154">Se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="380f4-154">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="380f4-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="380f4-158">Obtiene o establece un valor que indica si el motor de base de datos debe utilizar la memoria caché de archivos del sistema operativo para todos los archivos administrados.</span><span class="sxs-lookup"><span data-stu-id="380f4-158">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="380f4-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="380f4-162">Obtiene o establece un valor que indica si el motor de base de datos debe utilizar e/s de archivos asignados en memoria para los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-162">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span><span class="sxs-lookup"><span data-stu-id="380f4-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="380f4-166">Obtiene o establece el nivel de detalle de los mensajes de registro de eventos que el motor de base de datos emite al registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="380f4-166">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="380f4-167">Los números más altos producirán mensajes de registro de eventos más detallados.</span><span class="sxs-lookup"><span data-stu-id="380f4-167">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span><span class="sxs-lookup"><span data-stu-id="380f4-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="380f4-171">Obtiene o establece la codificación de valores que se debe hacer con las excepciones generadas en JET.</span><span class="sxs-lookup"><span data-stu-id="380f4-171">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span><span class="sxs-lookup"><span data-stu-id="380f4-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="380f4-175">Obtiene o establece el conjunto de acciones que deben realizarse en IOs que aparecen bloqueados.</span><span class="sxs-lookup"><span data-stu-id="380f4-175">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span><span class="sxs-lookup"><span data-stu-id="380f4-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="380f4-179">Obtiene o establece el umbral de lo que se considera una e/s bloqueada en la que se debe actuar.</span><span class="sxs-lookup"><span data-stu-id="380f4-179">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span><span class="sxs-lookup"><span data-stu-id="380f4-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="380f4-183">Obtiene el tamaño máximo de la clave.</span><span class="sxs-lookup"><span data-stu-id="380f4-183">Gets the maximum key size.</span></span> <span data-ttu-id="380f4-184">Esto depende de la versión de esent y del tamaño de página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-184">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="380f4-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="380f4-188">Obtiene o establece la compatibilidad con versiones anteriores de las convenciones de nomenclatura de los archivos de las versiones anteriores del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-188">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span><span class="sxs-lookup"><span data-stu-id="380f4-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="380f4-192">Obtiene el tamaño de fragmentos de LV.</span><span class="sxs-lookup"><span data-stu-id="380f4-192">Gets the lv chunks size.</span></span> <span data-ttu-id="380f4-193">Esto depende del tamaño de página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-193">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span><span class="sxs-lookup"><span data-stu-id="380f4-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="380f4-197">Obtiene o establece el número máximo de instancias que se pueden crear.</span><span class="sxs-lookup"><span data-stu-id="380f4-197">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span><span class="sxs-lookup"><span data-stu-id="380f4-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="380f4-201">Obtiene o establece la cantidad más pequeña de datos que se debe comprimir con la compresión Xpress.</span><span class="sxs-lookup"><span data-stu-id="380f4-201">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span><span class="sxs-lookup"><span data-stu-id="380f4-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="380f4-205">Este parámetro controla el número de operaciones de e/s de archivos de base de datos que se pueden poner en cola por disco en el sistema operativo host al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="380f4-205">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="380f4-206">Un valor mayor para este parámetro puede ayudar significativamente al rendimiento de una aplicación de base de datos grande.</span><span class="sxs-lookup"><span data-stu-id="380f4-206">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span><span class="sxs-lookup"><span data-stu-id="380f4-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="380f4-210">Obtiene o establece el nombre descriptivo para esta instancia del proceso.</span><span class="sxs-lookup"><span data-stu-id="380f4-210">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="380f4-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="380f4-214">Obtiene o establece el umbral en el que la caché de páginas de base de datos comienza a expulsar páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="380f4-214">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="380f4-215">Cuando el número de búferes de página en la memoria caché cae por debajo de este umbral, se iniciará un proceso en segundo plano para reponer ese grupo de búferes disponibles.</span><span class="sxs-lookup"><span data-stu-id="380f4-215">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="380f4-216">Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="380f4-216">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="380f4-217">Este umbral también debe ser siempre inferior al umbral de detención establecido por JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="380f4-217">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="380f4-218">El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de base de datos para generar los búferes disponibles antes de que la aplicación los necesite.</span><span class="sxs-lookup"><span data-stu-id="380f4-218">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="380f4-219">Un umbral de inicio alto proporcionará al proceso en segundo plano más tiempo para reaccionar.</span><span class="sxs-lookup"><span data-stu-id="380f4-219">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="380f4-220">Sin embargo, un umbral de inicio alto implica un umbral de detención mayor y reduce el tamaño efectivo de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-220">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="380f4-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="380f4-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="380f4-224">Obtiene o establece el umbral en el que la caché de páginas de base de datos termina la expulsión de las páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="380f4-224">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="380f4-225">Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer el grupo de búferes disponibles.</span><span class="sxs-lookup"><span data-stu-id="380f4-225">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="380f4-226">Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="380f4-226">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="380f4-227">Este umbral también debe ser siempre mayor que el umbral de inicio establecido por JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="380f4-227">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="380f4-228">La distancia entre el umbral de inicio y el umbral de detención afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-228">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="380f4-229">Una brecha más grande hará que sea más probable que se combinen las escrituras en páginas vecinas.</span><span class="sxs-lookup"><span data-stu-id="380f4-229">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="380f4-230">Sin embargo, un umbral de detención alta reducirá el tamaño efectivo de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="380f4-230">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="380f4-231">Superior</span><span class="sxs-lookup"><span data-stu-id="380f4-231">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="380f4-232">Vea también</span><span class="sxs-lookup"><span data-stu-id="380f4-232">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="380f4-233">Referencia</span><span class="sxs-lookup"><span data-stu-id="380f4-233">Reference</span></span>

[<span data-ttu-id="380f4-234">SystemParameters (clase)</span><span class="sxs-lookup"><span data-stu-id="380f4-234">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="380f4-235">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="380f4-235">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
