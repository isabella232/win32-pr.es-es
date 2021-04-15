---
title: Win32_RDMSVirtualDesktop (clase)
description: Representa un escritorio virtual.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSVirtualDesktop de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676708"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="c5df5-105">\_Clase Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="c5df5-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="c5df5-106">Representa un escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="c5df5-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c5df5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5df5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5df5-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="c5df5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5df5-109">Members</span></span>

<span data-ttu-id="c5df5-110">La **clase \_ RDMSVirtualDesktop de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c5df5-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="c5df5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5df5-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5df5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5df5-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5df5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5df5-113">Methods</span></span>

<span data-ttu-id="c5df5-114">La clase **Win32 \_ RDMSVirtualDesktop** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c5df5-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="c5df5-115">Método</span><span class="sxs-lookup"><span data-stu-id="c5df5-115">Method</span></span>                                                                                              | <span data-ttu-id="c5df5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5df5-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5df5-117">**GetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="c5df5-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="c5df5-118">Recupera el nombre de usuario y el nombre de dominio del usuario que está asignado al escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="c5df5-119">**GetVirtualDesktopAssignedToUser**</span><span class="sxs-lookup"><span data-stu-id="c5df5-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="c5df5-120">Recupera el escritorio virtual asignado al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="c5df5-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="c5df5-121">**GetVirtualDesktopDetails**</span><span class="sxs-lookup"><span data-stu-id="c5df5-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="c5df5-122">Recupera la información adicional sobre el escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="c5df5-123">**GetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="c5df5-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="c5df5-124">Recupera el estado del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="c5df5-125">**RemoveUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="c5df5-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="c5df5-126">Quita la asignación de usuario del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="c5df5-127">**SetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="c5df5-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="c5df5-128">Asigna un escritorio virtual a un usuario.</span><span class="sxs-lookup"><span data-stu-id="c5df5-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="c5df5-129">**SetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="c5df5-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="c5df5-130">Actualiza el estado del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="c5df5-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5df5-131">Properties</span></span>

<span data-ttu-id="c5df5-132">La **clase \_ RDMSVirtualDesktop de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c5df5-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5df5-133">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="c5df5-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-136">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5df5-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-137">Obtiene el alias de la colección de escritorios virtuales que administra la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="c5df5-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-141">Obtiene el nombre del equipo que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c5df5-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5df5-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-146">Obtiene el nombre de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-147">**SqlConnectionString**</span><span class="sxs-lookup"><span data-stu-id="c5df5-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-150">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5df5-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-151">Obtiene el estado de la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-152">**SessionUserName**</span><span class="sxs-lookup"><span data-stu-id="c5df5-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-155">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5df5-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-156">Obtiene el nombre de usuario del usuario que ha iniciado sesión en la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-157">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c5df5-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-158">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5df5-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-160">Obtiene el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-161">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="c5df5-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-164">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5df5-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-165">Obtiene el nombre de dominio del usuario que se asigna al escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="c5df5-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5df5-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-169">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5df5-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-170">Obtiene el nombre de usuario asignado al escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c5df5-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="c5df5-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5df5-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5df5-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5df5-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5df5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5df5-174">Obtiene el estado del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c5df5-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5df5-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5df5-175">Requirements</span></span>



| <span data-ttu-id="c5df5-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5df5-176">Requirement</span></span> | <span data-ttu-id="c5df5-177">Value</span><span class="sxs-lookup"><span data-stu-id="c5df5-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5df5-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5df5-178">Minimum supported client</span></span><br/> | <span data-ttu-id="c5df5-179">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c5df5-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c5df5-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5df5-180">Minimum supported server</span></span><br/> | <span data-ttu-id="c5df5-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5df5-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c5df5-182">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5df5-182">Namespace</span></span><br/>                | <span data-ttu-id="c5df5-183">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="c5df5-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c5df5-184">MOF</span><span class="sxs-lookup"><span data-stu-id="c5df5-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5df5-185"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5df5-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5df5-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5df5-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5df5-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5df5-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c5df5-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5df5-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5df5-189">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c5df5-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

