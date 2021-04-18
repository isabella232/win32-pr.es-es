---
title: Win32_VirtualDesktopSession (clase)
description: Administra una sesión de escritorio virtual.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_VirtualDesktopSession de clase, se describe
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489341"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="c650f-105">\_Clase Win32 VirtualDesktopSession</span><span class="sxs-lookup"><span data-stu-id="c650f-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="c650f-106">Administra una sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="c650f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c650f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c650f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c650f-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="c650f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c650f-109">Members</span></span>

<span data-ttu-id="c650f-110">La **clase \_ VirtualDesktopSession de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c650f-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="c650f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c650f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c650f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c650f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c650f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c650f-113">Methods</span></span>

<span data-ttu-id="c650f-114">La clase **Win32 \_ VirtualDesktopSession** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c650f-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="c650f-115">Método</span><span class="sxs-lookup"><span data-stu-id="c650f-115">Method</span></span>                                                         | <span data-ttu-id="c650f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c650f-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="c650f-117">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="c650f-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="c650f-118">Desconecta la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="c650f-119">**Forzado**</span><span class="sxs-lookup"><span data-stu-id="c650f-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="c650f-120">Cierra la sesión del usuario desde la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="c650f-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c650f-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="c650f-122">Envíe un mensaje al usuario a través de la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c650f-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c650f-123">Properties</span></span>

<span data-ttu-id="c650f-124">La **clase \_ VirtualDesktopSession de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c650f-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c650f-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="c650f-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c650f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c650f-128">Obtiene el nombre del equipo cliente que está conectado a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c650f-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-129">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="c650f-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c650f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c650f-132">Obtiene el nombre de la colección de escritorios virtuales que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-133">**ConnectState**</span><span class="sxs-lookup"><span data-stu-id="c650f-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c650f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c650f-136">Obtiene el estado de la conexión a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c650f-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-137">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c650f-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c650f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c650f-140">Obtiene el nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="c650f-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="c650f-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c650f-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c650f-144">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c650f-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c650f-145">Obtiene el identificador de la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-146">**UserName**</span><span class="sxs-lookup"><span data-stu-id="c650f-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c650f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c650f-149">Obtiene el nombre de la cuenta de usuario que está asignada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c650f-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="c650f-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c650f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c650f-153">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c650f-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c650f-154">Obtiene el nombre del servidor host de virtualización Escritorio remoto que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c650f-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c650f-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="c650f-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c650f-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c650f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c650f-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c650f-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c650f-158">Obtiene el nombre de la máquina virtual que está asignada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c650f-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c650f-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c650f-159">Requirements</span></span>



| <span data-ttu-id="c650f-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="c650f-160">Requirement</span></span> | <span data-ttu-id="c650f-161">Value</span><span class="sxs-lookup"><span data-stu-id="c650f-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c650f-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c650f-162">Minimum supported client</span></span><br/> | <span data-ttu-id="c650f-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c650f-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c650f-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c650f-164">Minimum supported server</span></span><br/> | <span data-ttu-id="c650f-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c650f-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c650f-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c650f-166">Namespace</span></span><br/>                | <span data-ttu-id="c650f-167">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="c650f-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c650f-168">MOF</span><span class="sxs-lookup"><span data-stu-id="c650f-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c650f-169"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c650f-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c650f-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c650f-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c650f-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c650f-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c650f-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="c650f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c650f-173">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c650f-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

