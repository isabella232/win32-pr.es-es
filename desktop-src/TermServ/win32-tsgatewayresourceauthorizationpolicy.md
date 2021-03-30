---
title: Win32_TSGatewayResourceAuthorizationPolicy (clase)
description: Describe una Escritorio remoto Directiva de autorización de recursos (RD \ 160; RAP). Un RD \ 160; RAP se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de Escritorio remoto puerta de enlace de escritorio remoto.
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayResourceAuthorizationPolicy de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079294"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="546d8-106">\_Clase Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="546d8-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="546d8-107">Describe una Escritorio remoto Directiva de autorización de recursos (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="546d8-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="546d8-108">Una RAP de RD se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de Escritorio remoto puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="546d8-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="546d8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="546d8-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="546d8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="546d8-110">Members</span></span>

<span data-ttu-id="546d8-111">La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="546d8-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="546d8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="546d8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="546d8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="546d8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="546d8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="546d8-114">Methods</span></span>

<span data-ttu-id="546d8-115">La clase **Win32 \_ TSGatewayResourceAuthorizationPolicy** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="546d8-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="546d8-116">Método</span><span class="sxs-lookup"><span data-stu-id="546d8-116">Method</span></span>                                                                                          | <span data-ttu-id="546d8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="546d8-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="546d8-118">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="546d8-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="546d8-119">Agrega los nombres de grupos de usuarios especificados a los grupos de usuarios existentes en la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="546d8-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="546d8-120">**A**</span><span class="sxs-lookup"><span data-stu-id="546d8-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="546d8-121">Crea una RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="546d8-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="546d8-122">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="546d8-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="546d8-123">Elimina la RAP de RD actual.</span><span class="sxs-lookup"><span data-stu-id="546d8-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="546d8-124">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="546d8-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="546d8-125">Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="546d8-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="546d8-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="546d8-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="546d8-127">Establece la propiedad **Description** para la rap de Rd.</span><span class="sxs-lookup"><span data-stu-id="546d8-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="546d8-128">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="546d8-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="546d8-129">Habilita o deshabilita la RAP de RD estableciendo la propiedad **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="546d8-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="546d8-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="546d8-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="546d8-131">Establece la propiedad de **nombre** para la rap de Rd.</span><span class="sxs-lookup"><span data-stu-id="546d8-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="546d8-132">**SetPortNumbers**</span><span class="sxs-lookup"><span data-stu-id="546d8-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="546d8-133">Establece la propiedad **PortNumbers** para la rap de Rd.</span><span class="sxs-lookup"><span data-stu-id="546d8-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="546d8-134">**SetResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="546d8-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="546d8-135">Establece las propiedades **ResourceGroupType** y **ResourceGroupName** .</span><span class="sxs-lookup"><span data-stu-id="546d8-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="546d8-136">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="546d8-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="546d8-137">Establece la propiedad **UserGroupNames** para la rap de Rd.</span><span class="sxs-lookup"><span data-stu-id="546d8-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="546d8-138">**Update**</span><span class="sxs-lookup"><span data-stu-id="546d8-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="546d8-139">Actualiza la RAP de RD actual.</span><span class="sxs-lookup"><span data-stu-id="546d8-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="546d8-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="546d8-140">Properties</span></span>

<span data-ttu-id="546d8-141">La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="546d8-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="546d8-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="546d8-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-145">Descripción de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="546d8-145">Description of the RD RAP.</span></span> <span data-ttu-id="546d8-146">Esta propiedad se cambia con el método [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-147">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="546d8-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="546d8-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-150">Indica si esta RAP de RD está habilitada.</span><span class="sxs-lookup"><span data-stu-id="546d8-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="546d8-151">Esta propiedad se cambia con el método [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="546d8-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="546d8-155">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="546d8-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="546d8-156">Nombre de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="546d8-156">Name of the RD RAP.</span></span> <span data-ttu-id="546d8-157">Esta propiedad se cambia con el método [**setName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-158">**PortNumbers**</span><span class="sxs-lookup"><span data-stu-id="546d8-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-161">Lista de números de Puerto separados por punto y coma que se permiten para esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="546d8-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="546d8-162">Para permitir cualquier número de puerto, establezca " \* ".</span><span class="sxs-lookup"><span data-stu-id="546d8-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="546d8-163">**ProtocolNames**</span><span class="sxs-lookup"><span data-stu-id="546d8-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-166">Lista de nombres de protocolos separados por punto y coma que están habilitados para esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="546d8-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="546d8-167">Los nombres deben coincidir con el valor devuelto del método [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-168">**ResourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="546d8-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-171">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="546d8-171">Resource group name.</span></span> <span data-ttu-id="546d8-172">Esta propiedad se cambia con el método [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-173">**ResourceGroupType**</span><span class="sxs-lookup"><span data-stu-id="546d8-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-176">Identifica el tipo del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="546d8-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="546d8-177">Esta propiedad se cambia con el método [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="546d8-178">RG</span><span class="sxs-lookup"><span data-stu-id="546d8-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="546d8-179">Un grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="546d8-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-180">CG</span><span class="sxs-lookup"><span data-stu-id="546d8-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="546d8-181">Grupo de equipos, tal como se almacena en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="546d8-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="546d8-182">TODOS</span><span class="sxs-lookup"><span data-stu-id="546d8-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="546d8-183">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="546d8-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="546d8-184">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="546d8-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="546d8-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="546d8-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="546d8-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="546d8-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="546d8-187">Lista separada por puntos y comas de nombres de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="546d8-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="546d8-188">Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso.</span><span class="sxs-lookup"><span data-stu-id="546d8-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="546d8-189">Esta propiedad se cambia con los métodos [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)y [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="546d8-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="546d8-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="546d8-190">Remarks</span></span>

<span data-ttu-id="546d8-191">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="546d8-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="546d8-192">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="546d8-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="546d8-193">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="546d8-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="546d8-194">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="546d8-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="546d8-195">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="546d8-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="546d8-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="546d8-196">Requirements</span></span>



| <span data-ttu-id="546d8-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="546d8-197">Requirement</span></span> | <span data-ttu-id="546d8-198">Value</span><span class="sxs-lookup"><span data-stu-id="546d8-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="546d8-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="546d8-199">Minimum supported client</span></span><br/> | <span data-ttu-id="546d8-200">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="546d8-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="546d8-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="546d8-201">Minimum supported server</span></span><br/> | <span data-ttu-id="546d8-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="546d8-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="546d8-203">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="546d8-203">Namespace</span></span><br/>                | <span data-ttu-id="546d8-204">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="546d8-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="546d8-205">MOF</span><span class="sxs-lookup"><span data-stu-id="546d8-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="546d8-206"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="546d8-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="546d8-207">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="546d8-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="546d8-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="546d8-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="546d8-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="546d8-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546d8-210">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="546d8-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="546d8-211">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="546d8-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="546d8-212">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="546d8-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="546d8-213">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="546d8-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="546d8-214">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="546d8-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="546d8-215">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="546d8-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

