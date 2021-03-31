---
title: Win32_SessionDirectoryVMMPlugin (clase)
description: Representa un complemento de Virtual Machine Manager (VMM) registrado con un agente de sesiones.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryVMMPlugin de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996073"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="b08f3-105">\_Clase Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="b08f3-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="b08f3-106">Representa un complemento de Virtual Machine Manager (VMM) registrado con un agente de sesiones.</span><span class="sxs-lookup"><span data-stu-id="b08f3-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="b08f3-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b08f3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08f3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b08f3-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="b08f3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b08f3-109">Members</span></span>

<span data-ttu-id="b08f3-110">La **clase \_ SessionDirectoryVMMPlugin de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b08f3-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="b08f3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b08f3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b08f3-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b08f3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b08f3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b08f3-113">Methods</span></span>

<span data-ttu-id="b08f3-114">La clase **Win32 \_ SessionDirectoryVMMPlugin** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b08f3-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="b08f3-115">Método</span><span class="sxs-lookup"><span data-stu-id="b08f3-115">Method</span></span>                                                                             | <span data-ttu-id="b08f3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b08f3-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="b08f3-117">**GetCurrentVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="b08f3-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="b08f3-118">Obtiene el complemento de prioridad máxima que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b08f3-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="b08f3-119">**RegisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="b08f3-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="b08f3-120">Registra un nuevo complemento de VMM.</span><span class="sxs-lookup"><span data-stu-id="b08f3-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="b08f3-121">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="b08f3-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="b08f3-122">Habilita o deshabilita el complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="b08f3-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="b08f3-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="b08f3-124">Establece el nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="b08f3-125">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="b08f3-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="b08f3-126">Establece la prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="b08f3-127">**SetProvider**</span><span class="sxs-lookup"><span data-stu-id="b08f3-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="b08f3-128">Establece el nombre del proveedor del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="b08f3-129">**SetServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="b08f3-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="b08f3-130">Establece la ubicación del servicio del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="b08f3-131">**UnregisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="b08f3-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="b08f3-132">Anula el registro del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="b08f3-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b08f3-133">Properties</span></span>

<span data-ttu-id="b08f3-134">La **clase \_ SessionDirectoryVMMPlugin de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b08f3-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b08f3-135">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="b08f3-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b08f3-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b08f3-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b08f3-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b08f3-138">Indica si el complemento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b08f3-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="b08f3-139">**True** si el complemento está habilitado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b08f3-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="b08f3-140">El complemento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b08f3-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="b08f3-141">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="b08f3-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b08f3-142">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b08f3-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b08f3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-144">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b08f3-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b08f3-145">Prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-145">The priority of the plug-in.</span></span> <span data-ttu-id="b08f3-146">Cuanto mayor sea el valor, mayor será la prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="b08f3-147">De forma predeterminada, la prioridad es cero.</span><span class="sxs-lookup"><span data-stu-id="b08f3-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="b08f3-148">**sClassID**</span><span class="sxs-lookup"><span data-stu-id="b08f3-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b08f3-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b08f3-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b08f3-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b08f3-151">Identificador de clase del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="b08f3-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="b08f3-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b08f3-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b08f3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b08f3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b08f3-155">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="b08f3-156">**sProvider**</span><span class="sxs-lookup"><span data-stu-id="b08f3-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b08f3-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b08f3-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b08f3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b08f3-159">Nombre del proveedor del complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="b08f3-160">**sServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="b08f3-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b08f3-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b08f3-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b08f3-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b08f3-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b08f3-163">La ubicación del servicio en la que debe ponerse en contacto el complemento.</span><span class="sxs-lookup"><span data-stu-id="b08f3-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b08f3-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b08f3-164">Requirements</span></span>



| <span data-ttu-id="b08f3-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b08f3-165">Requirement</span></span> | <span data-ttu-id="b08f3-166">Value</span><span class="sxs-lookup"><span data-stu-id="b08f3-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b08f3-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b08f3-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b08f3-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b08f3-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b08f3-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b08f3-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b08f3-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b08f3-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b08f3-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b08f3-171">Namespace</span></span><br/>                | <span data-ttu-id="b08f3-172">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b08f3-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b08f3-173">MOF</span><span class="sxs-lookup"><span data-stu-id="b08f3-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b08f3-174"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b08f3-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b08f3-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b08f3-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b08f3-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b08f3-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

