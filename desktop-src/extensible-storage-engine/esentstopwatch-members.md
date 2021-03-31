---
description: 'Más información acerca de: miembros de EsentStopwatch'
title: Miembros de EsentStopwatch
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815675"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="ec027-103">Miembros de EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="ec027-103">EsentStopwatch members</span></span>

<span data-ttu-id="ec027-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="ec027-104">Include protected members</span></span>  
<span data-ttu-id="ec027-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="ec027-105">Include inherited members</span></span>  

<span data-ttu-id="ec027-106">Proporciona un conjunto de métodos y propiedades que puede usar para medir las estadísticas de trabajo ESENT de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="ec027-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="ec027-107">Si la versión actual de ESENT no es compatible con [JetGetThreadStats (JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) , todas las estadísticas de esent serán 0.</span><span class="sxs-lookup"><span data-stu-id="ec027-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="ec027-108">El tipo [EsentStopwatch](./esentstopwatch-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="ec027-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ec027-109">Constructores</span><span class="sxs-lookup"><span data-stu-id="ec027-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ec027-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec027-110">Name</span></span></th>
<th><span data-ttu-id="ec027-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec027-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span><span class="sxs-lookup"><span data-stu-id="ec027-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec027-114">Superior</span><span class="sxs-lookup"><span data-stu-id="ec027-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ec027-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec027-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ec027-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec027-116">Name</span></span></th>
<th><span data-ttu-id="ec027-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec027-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ec027-119"><a href="dn334934(v=exchg.10).md">Transcurrido</a></span><span class="sxs-lookup"><span data-stu-id="ec027-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="ec027-120">Obtiene el tiempo total transcurrido medido por la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="ec027-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ec027-122"><a href="dn334933(v=exchg.10).md">IsRunning (</a></span><span class="sxs-lookup"><span data-stu-id="ec027-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="ec027-123">Obtiene un valor que indica si el temporizador de EsentStopwatch se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ec027-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ec027-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span><span class="sxs-lookup"><span data-stu-id="ec027-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="ec027-126">Obtiene el total de estadísticas de trabajo de ESENT medida por la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="ec027-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec027-127">Superior</span><span class="sxs-lookup"><span data-stu-id="ec027-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ec027-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec027-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ec027-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec027-129">Name</span></span></th>
<th><span data-ttu-id="ec027-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec027-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="ec027-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ec027-133">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ec027-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="ec027-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="ec027-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ec027-136">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ec027-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ec027-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ec027-139">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ec027-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ec027-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ec027-142">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ec027-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="ec027-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="ec027-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ec027-145">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ec027-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-147"><a href="dn334869(v=exchg.10).md">Reset</a></span><span class="sxs-lookup"><span data-stu-id="ec027-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="ec027-148">Detiene la medición del intervalo de tiempo y restablece las estadísticas del subproceso.</span><span class="sxs-lookup"><span data-stu-id="ec027-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-150"><a href="dn334931(v=exchg.10).md">Iniciar</a></span><span class="sxs-lookup"><span data-stu-id="ec027-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="ec027-151">Comienza a medir el trabajo ESENT.</span><span class="sxs-lookup"><span data-stu-id="ec027-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="ec027-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span><span class="sxs-lookup"><span data-stu-id="ec027-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="ec027-155">Inicializa una nueva instancia de EsentStopwatch y comienza a medir el tiempo transcurrido.</span><span class="sxs-lookup"><span data-stu-id="ec027-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-157"><a href="dn334932(v=exchg.10).md">Detención</a></span><span class="sxs-lookup"><span data-stu-id="ec027-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="ec027-158">Detiene la medición del trabajo ESENT.</span><span class="sxs-lookup"><span data-stu-id="ec027-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ec027-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ec027-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ec027-161">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="/dotnet/api/system.diagnostics.stopwatch">cronómetro</a>actual.</span><span class="sxs-lookup"><span data-stu-id="ec027-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="ec027-162">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="ec027-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec027-163">Superior</span><span class="sxs-lookup"><span data-stu-id="ec027-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ec027-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec027-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec027-165">Referencia</span><span class="sxs-lookup"><span data-stu-id="ec027-165">Reference</span></span>

[<span data-ttu-id="ec027-166">Clase EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="ec027-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="ec027-167">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ec027-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
