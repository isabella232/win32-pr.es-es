---
description: 'Más información acerca de: miembros de instancia'
title: Miembros de instancia
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8ba8dad079feba566dbb8fca873fcea19af778ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908266"
---
# <a name="instance-members"></a><span data-ttu-id="eb4e6-103">Miembros de instancia</span><span class="sxs-lookup"><span data-stu-id="eb4e6-103">Instance members</span></span>

<span data-ttu-id="eb4e6-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="eb4e6-104">Include protected members</span></span>  
<span data-ttu-id="eb4e6-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="eb4e6-105">Include inherited members</span></span>  

<span data-ttu-id="eb4e6-106">Una clase que encapsula una [JET_INSTANCE](./jet-instance-structure.md) en un objeto descartable.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-106">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="eb4e6-107">La instancia debe cerrarse en último lugar y el cierre de la instancia libera todos los demás recursos de la instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-107">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

<span data-ttu-id="eb4e6-108">El tipo de [instancia](./instance-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-108">The [Instance](./instance-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="eb4e6-109">Constructores</span><span class="sxs-lookup"><span data-stu-id="eb4e6-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eb4e6-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb4e6-110">Name</span></span></th>
<th><span data-ttu-id="eb4e6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb4e6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-113"><a href="dn350924(v=exchg.10).md">Instancia (cadena)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-113"><a href="dn350924(v=exchg.10).md">Instance(String)</a></span></span></td>
<td><span data-ttu-id="eb4e6-114">Inicializa una nueva instancia de la clase de instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-114">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="eb4e6-115">La JET_INSTANCE subyacente está asignada, pero no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-115">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-117"><a href="dn350927(v=exchg.10).md">Instancia (cadena, cadena)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-117"><a href="dn350927(v=exchg.10).md">Instance(String, String)</a></span></span></td>
<td><span data-ttu-id="eb4e6-118">Inicializa una nueva instancia de la clase de instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-118">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="eb4e6-119">La JET_INSTANCE subyacente está asignada, pero no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-119">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-121"><a href="dn350948(v=exchg.10).md">Instancia (cadena, cadena, TermGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-121"><a href="dn350948(v=exchg.10).md">Instance(String, String, TermGrbit)</a></span></span></td>
<td><span data-ttu-id="eb4e6-122">Inicializa una nueva instancia de la clase de instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-122">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="eb4e6-123">La JET_INSTANCE subyacente está asignada, pero no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-123">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb4e6-124">Superior</span><span class="sxs-lookup"><span data-stu-id="eb4e6-124">Top</span></span>

## <a name="properties"></a><span data-ttu-id="eb4e6-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb4e6-125">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eb4e6-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb4e6-126">Name</span></span></th>
<th><span data-ttu-id="eb4e6-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb4e6-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="eb4e6-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span></span></td>
<td><span data-ttu-id="eb4e6-130">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-130">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="eb4e6-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span></span></td>
<td><span data-ttu-id="eb4e6-133">(Se hereda de <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-133">(Inherited from <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="eb4e6-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span></span></td>
<td><span data-ttu-id="eb4e6-136">Obtiene el JET_INSTANCE que esta instancia contiene.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-136">Gets the JET_INSTANCE that this instance contains.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="eb4e6-138"><a href="dn350962(v=exchg.10).md">Parámetros</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-138"><a href="dn350962(v=exchg.10).md">Parameters</a></span></span></td>
<td><span data-ttu-id="eb4e6-139">Obtiene el InstanceParameters para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-139">Gets the InstanceParameters for this instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="eb4e6-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span></span></td>
<td><span data-ttu-id="eb4e6-142">Obtiene o establece el TermGrbit para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-142">Gets or sets the TermGrbit for this instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb4e6-143">Superior</span><span class="sxs-lookup"><span data-stu-id="eb4e6-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="eb4e6-144">Métodos</span><span class="sxs-lookup"><span data-stu-id="eb4e6-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eb4e6-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb4e6-145">Name</span></span></th>
<th><span data-ttu-id="eb4e6-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb4e6-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Cerrar</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span></span></td>
<td><span data-ttu-id="eb4e6-149">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-149">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span></span></td>
<td><span data-ttu-id="eb4e6-152">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-152">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span></span></td>
<td><span data-ttu-id="eb4e6-155">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-155">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span></span></td>
<td><span data-ttu-id="eb4e6-158">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-158">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="eb4e6-161">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-161">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="eb4e6-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="eb4e6-164">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-164">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="eb4e6-167">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="eb4e6-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="eb4e6-170">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-170">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="eb4e6-173">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="eb4e6-176">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-176">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-178"><a href="dn350932(v=exchg.10).md">Init ()</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-178"><a href="dn350932(v=exchg.10).md">Init()</a></span></span></td>
<td><span data-ttu-id="eb4e6-179">Inicialice el JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-179">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-181"><a href="dn350954(v=exchg.10).md">Init (InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-181"><a href="dn350954(v=exchg.10).md">Init(InitGrbit)</a></span></span></td>
<td><span data-ttu-id="eb4e6-182">Inicialice el JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-182">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-184"><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-184"><a href="dn350934(v=exchg.10).md">Init(JET_RSTINFO, InitGrbit)</a></span></span></td>
<td><span data-ttu-id="eb4e6-185">Inicialice el JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-185">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="eb4e6-186">Esta API requiere al menos la versión de vista de ESENT.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-186">This API requires at least the Vista version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="eb4e6-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="eb4e6-189">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-189">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="eb4e6-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span></span></td>
<td><span data-ttu-id="eb4e6-192">Libera el identificador de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-192">Release the handle for this instance.</span></span> <span data-ttu-id="eb4e6-193">(Invalida <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-193">(Overrides <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle.ReleaseHandle()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="eb4e6-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span></span></td>
<td><span data-ttu-id="eb4e6-196">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-196">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span></span></td>
<td><span data-ttu-id="eb4e6-199">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-199">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-201"><a href="dn350935(v=exchg.10).md">Término</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-201"><a href="dn350935(v=exchg.10).md">Term</a></span></span></td>
<td><span data-ttu-id="eb4e6-202">Finalice el JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-202">Terminate the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="eb4e6-204"><a href="dn350960(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-204"><a href="dn350960(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="eb4e6-205">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa la <a href="dn350923(v=exchg.10).md">instancia</a>actual.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-205">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350923(v=exchg.10).md">Instance</a>.</span></span> <span data-ttu-id="eb4e6-206">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-206">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb4e6-207">Superior</span><span class="sxs-lookup"><span data-stu-id="eb4e6-207">Top</span></span>

## <a name="operators"></a><span data-ttu-id="eb4e6-208">Operadores</span><span class="sxs-lookup"><span data-stu-id="eb4e6-208">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eb4e6-209">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb4e6-209">Name</span></span></th>
<th><span data-ttu-id="eb4e6-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb4e6-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="eb4e6-213"><a href="dn350950(v=exchg.10).md">Implicit (instancia a JET_INSTANCE)</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-213"><a href="dn350950(v=exchg.10).md">Implicit(Instance to JET_INSTANCE)</a></span></span></td>
<td><span data-ttu-id="eb4e6-214">Proporcionar la conversión implícita de un objeto de instancia a una estructura de JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-214">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="eb4e6-215">Esto se hace para que se pueda usar una instancia en cualquier lugar en el que se requiera JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-215">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb4e6-216">Superior</span><span class="sxs-lookup"><span data-stu-id="eb4e6-216">Top</span></span>

## <a name="fields"></a><span data-ttu-id="eb4e6-217">Campos</span><span class="sxs-lookup"><span data-stu-id="eb4e6-217">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eb4e6-218">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb4e6-218">Name</span></span></th>
<th><span data-ttu-id="eb4e6-219">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb4e6-219">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Campo protegido" alt="Protected field" /></td>
<td><span data-ttu-id="eb4e6-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">asa</a></span><span class="sxs-lookup"><span data-stu-id="eb4e6-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">handle</a></span></span></td>
<td><span data-ttu-id="eb4e6-222">(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>).</span><span class="sxs-lookup"><span data-stu-id="eb4e6-222">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb4e6-223">Superior</span><span class="sxs-lookup"><span data-stu-id="eb4e6-223">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="eb4e6-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb4e6-224">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb4e6-225">Referencia</span><span class="sxs-lookup"><span data-stu-id="eb4e6-225">Reference</span></span>

[<span data-ttu-id="eb4e6-226">Clase de instancia</span><span class="sxs-lookup"><span data-stu-id="eb4e6-226">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="eb4e6-227">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eb4e6-227">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
