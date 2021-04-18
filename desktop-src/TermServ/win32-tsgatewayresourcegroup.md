---
title: Win32_TSGatewayResourceGroup (clase)
description: Describe un grupo de recursos, que asigna un conjunto de recursos (nombres de equipo) a una sola entidad.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayResourceGroup de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685959"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="eceee-105">\_Clase Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eceee-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="eceee-106">Describe un grupo de recursos, que asigna un conjunto de recursos (nombres de equipo) a una sola entidad.</span><span class="sxs-lookup"><span data-stu-id="eceee-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="eceee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eceee-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="eceee-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="eceee-108">Members</span></span>

<span data-ttu-id="eceee-109">La **clase \_ TSGatewayResourceGroup de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eceee-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="eceee-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="eceee-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="eceee-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eceee-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eceee-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="eceee-112">Methods</span></span>

<span data-ttu-id="eceee-113">La clase **Win32 \_ TSGatewayResourceGroup** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="eceee-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="eceee-114">Método</span><span class="sxs-lookup"><span data-stu-id="eceee-114">Method</span></span>                                                                  | <span data-ttu-id="eceee-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="eceee-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="eceee-116">**AddResources**</span><span class="sxs-lookup"><span data-stu-id="eceee-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="eceee-117">Agrega recursos a la propiedad **Resources** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="eceee-118">**A**</span><span class="sxs-lookup"><span data-stu-id="eceee-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="eceee-119">Crea un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="eceee-120">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="eceee-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="eceee-121">Elimina este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="eceee-122">**RemoveResources**</span><span class="sxs-lookup"><span data-stu-id="eceee-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="eceee-123">Elimina recursos de la propiedad **Resources** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="eceee-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="eceee-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="eceee-125">Establece la propiedad **Description** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="eceee-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="eceee-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="eceee-127">Establece la propiedad de **nombre** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="eceee-128">**SetResources**</span><span class="sxs-lookup"><span data-stu-id="eceee-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="eceee-129">Establece la propiedad **Resources** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="eceee-130">**Update**</span><span class="sxs-lookup"><span data-stu-id="eceee-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="eceee-131">Actualiza este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="eceee-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eceee-132">Properties</span></span>

<span data-ttu-id="eceee-133">La **clase \_ TSGatewayResourceGroup de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eceee-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eceee-134">**AssociatedRAPs**</span><span class="sxs-lookup"><span data-stu-id="eceee-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eceee-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eceee-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eceee-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eceee-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eceee-137">Lista separada por punto y coma de Servicios de Escritorio remoto directivas de autorización de recursos (RAP de RD) que están asociadas a este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="eceee-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eceee-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eceee-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eceee-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eceee-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eceee-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eceee-141">Descripción del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-141">Description of the resource group.</span></span> <span data-ttu-id="eceee-142">Esta propiedad se puede cambiar con el método [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="eceee-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="eceee-143">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="eceee-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eceee-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eceee-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eceee-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eceee-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eceee-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eceee-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eceee-147">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-147">Name of the resource group.</span></span> <span data-ttu-id="eceee-148">Esta propiedad se puede cambiar con el método [**setName**](setname-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="eceee-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="eceee-149">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="eceee-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eceee-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eceee-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eceee-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eceee-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eceee-152">Lista de recursos separados por punto y coma en este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="eceee-153">Un " \* " hace referencia a todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="eceee-153">An "\*" means all resources.</span></span> <span data-ttu-id="eceee-154">Esta propiedad se puede cambiar con los métodos [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)y [**Update**](update-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="eceee-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eceee-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eceee-155">Remarks</span></span>

<span data-ttu-id="eceee-156">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="eceee-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="eceee-157">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eceee-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eceee-158">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eceee-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eceee-159">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="eceee-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eceee-160">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eceee-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eceee-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eceee-161">Requirements</span></span>



| <span data-ttu-id="eceee-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="eceee-162">Requirement</span></span> | <span data-ttu-id="eceee-163">Value</span><span class="sxs-lookup"><span data-stu-id="eceee-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eceee-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eceee-164">Minimum supported client</span></span><br/> | <span data-ttu-id="eceee-165">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eceee-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="eceee-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eceee-166">Minimum supported server</span></span><br/> | <span data-ttu-id="eceee-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eceee-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eceee-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eceee-168">Namespace</span></span><br/>                | <span data-ttu-id="eceee-169">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="eceee-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="eceee-170">MOF</span><span class="sxs-lookup"><span data-stu-id="eceee-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eceee-171"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eceee-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="eceee-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eceee-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eceee-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eceee-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eceee-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="eceee-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eceee-175">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="eceee-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="eceee-176">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="eceee-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="eceee-177">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="eceee-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="eceee-178">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="eceee-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="eceee-179">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="eceee-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="eceee-180">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="eceee-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

