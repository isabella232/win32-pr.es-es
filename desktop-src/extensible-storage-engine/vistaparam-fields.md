---
description: 'Más información acerca de: campos VistaParam'
title: Campos VistaParam (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6e20c4b784b9a4421c447f24d5736d7c6ef67f41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567432"
---
# <a name="vistaparam-fields"></a><span data-ttu-id="90c67-103">Campos de VistaParam</span><span class="sxs-lookup"><span data-stu-id="90c67-103">VistaParam fields</span></span>

<span data-ttu-id="90c67-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="90c67-104">Include protected members</span></span>  
<span data-ttu-id="90c67-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="90c67-105">Include inherited members</span></span>  

<span data-ttu-id="90c67-106">El tipo [VistaParam](./vistaparam-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="90c67-106">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="90c67-107">Campos</span><span class="sxs-lookup"><span data-stu-id="90c67-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="90c67-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="90c67-108">Name</span></span></th>
<th><span data-ttu-id="90c67-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="90c67-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="90c67-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="90c67-113">Este parámetro controla el número de recursos de árbol B + almacenados en memoria caché por la instancia de después de que la aplicación haya cerrado las tablas que representan.</span><span class="sxs-lookup"><span data-stu-id="90c67-113">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="90c67-114">Los valores grandes de este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="90c67-114">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="90c67-115">Esto resulta útil para las aplicaciones que tienen un esquema con un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="90c67-115">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-118"><a href="dn335289(v=exchg.10).md">Configuración</a></span><span class="sxs-lookup"><span data-stu-id="90c67-118"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="90c67-119">Este parámetro expone varios conjuntos de valores predeterminados para todo el conjunto de parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="90c67-119">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="90c67-120">Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración.</span><span class="sxs-lookup"><span data-stu-id="90c67-120">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="90c67-121">Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="90c67-121">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="90c67-122">Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="90c67-122">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="90c67-123">Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.</span><span class="sxs-lookup"><span data-stu-id="90c67-123">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="90c67-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="90c67-127">Este parámetro se usa para controlar el momento en que el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="90c67-127">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="90c67-128">Este parámetro se usa junto con la <a href="dn335289(v=exchg.10).md">configuración</a> para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada.</span><span class="sxs-lookup"><span data-stu-id="90c67-128">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="90c67-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="90c67-132">Habilita el uso de la caché de archivos del sistema operativo para todos los archivos administrados.</span><span class="sxs-lookup"><span data-stu-id="90c67-132">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="90c67-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="90c67-136">Habilitar el uso de e/s de archivos asignados en memoria para los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="90c67-136">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-139"><a href="dn335292(v=exchg.10).md">KeyMost</a></span><span class="sxs-lookup"><span data-stu-id="90c67-139"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="90c67-140">Este parámetro de solo lectura indica la longitud máxima permitida de la clave de índice que se puede seleccionar para el tamaño de página de la base de datos actual (tal y como se configura mediante <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="90c67-140">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="90c67-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="90c67-144">Este parámetro proporciona compatibilidad con versiones anteriores de las convenciones de nomenclatura de los archivos de las versiones anteriores del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="90c67-144">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="90c67-148">Establezca el nombre asociado a la clase de tabla 10.</span><span class="sxs-lookup"><span data-stu-id="90c67-148">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="90c67-152">Establezca el nombre asociado a la clase de tabla 11.</span><span class="sxs-lookup"><span data-stu-id="90c67-152">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="90c67-156">Establezca el nombre asociado a la clase de tabla 12.</span><span class="sxs-lookup"><span data-stu-id="90c67-156">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="90c67-160">Establezca el nombre asociado a la clase de tabla 13.</span><span class="sxs-lookup"><span data-stu-id="90c67-160">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="90c67-164">Establezca el nombre asociado a la clase de tabla 14.</span><span class="sxs-lookup"><span data-stu-id="90c67-164">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="90c67-168">Establezca el nombre asociado a la clase de tabla 15.</span><span class="sxs-lookup"><span data-stu-id="90c67-168">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="90c67-172">Establezca el nombre asociado a la clase de tabla 1.</span><span class="sxs-lookup"><span data-stu-id="90c67-172">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="90c67-176">Establezca el nombre asociado a la clase de tabla 2.</span><span class="sxs-lookup"><span data-stu-id="90c67-176">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="90c67-180">Establezca el nombre asociado a la clase de tabla 3.</span><span class="sxs-lookup"><span data-stu-id="90c67-180">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="90c67-184">Establezca el nombre asociado a la clase de tabla 4.</span><span class="sxs-lookup"><span data-stu-id="90c67-184">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="90c67-188">Establezca el nombre asociado a la clase de tabla 5.</span><span class="sxs-lookup"><span data-stu-id="90c67-188">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="90c67-192">Establezca el nombre asociado a la clase de tabla 6.</span><span class="sxs-lookup"><span data-stu-id="90c67-192">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="90c67-196">Establezca el nombre asociado a la clase de tabla 7.</span><span class="sxs-lookup"><span data-stu-id="90c67-196">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="90c67-200">Establezca el nombre asociado a la clase de tabla 8.</span><span class="sxs-lookup"><span data-stu-id="90c67-200">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="90c67-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="90c67-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="90c67-204">Establezca el nombre asociado a la clase de tabla 9.</span><span class="sxs-lookup"><span data-stu-id="90c67-204">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90c67-205">Superior</span><span class="sxs-lookup"><span data-stu-id="90c67-205">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="90c67-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="90c67-206">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90c67-207">Referencia</span><span class="sxs-lookup"><span data-stu-id="90c67-207">Reference</span></span>

[<span data-ttu-id="90c67-208">Clase VistaParam</span><span class="sxs-lookup"><span data-stu-id="90c67-208">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="90c67-209">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="90c67-209">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
