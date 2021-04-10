---
title: Método Update de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Actualiza la Directiva de autorización de recursos de Escritorio remoto actual (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Método Update Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Servicios de Escritorio remoto de clase Win32_TSGatewayResourceAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150486"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="60379-106">Método Update de la \_ clase Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="60379-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="60379-107">Actualiza la Directiva de autorización de recursos de Escritorio remoto actual (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="60379-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="60379-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60379-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="60379-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60379-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60379-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="60379-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-111">Nombre de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="60379-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="60379-112">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="60379-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-113">Descripción de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="60379-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="60379-114">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60379-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-115">Indica si se debe habilitar la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="60379-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="60379-116">*ResourceGroupName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60379-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-117">Nombre del grupo de recursos asociado a esta RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="60379-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="60379-118">*ResourceGroupType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60379-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-119">Tipo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60379-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="60379-120">RG</span><span class="sxs-lookup"><span data-stu-id="60379-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="60379-121">Un grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="60379-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="60379-122">CG</span><span class="sxs-lookup"><span data-stu-id="60379-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="60379-123">Grupo de equipos, tal como se almacena en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="60379-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="60379-124">TODOS</span><span class="sxs-lookup"><span data-stu-id="60379-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="60379-125">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="60379-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="60379-126">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60379-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-127">Lista separada por puntos y comas de nombres de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="60379-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="60379-128">Los nombres tienen el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="60379-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="60379-129">Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso.</span><span class="sxs-lookup"><span data-stu-id="60379-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="60379-130">*ProtocolNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60379-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-131">Lista separada por puntos y comas de nombres de protocolo que están habilitados para esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="60379-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="60379-132">Los nombres deben coincidir con el valor devuelto del método [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="60379-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="60379-133">*PortNumbers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60379-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60379-134">Lista separada por puntos y comas de números de puerto que están habilitados para esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="60379-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="60379-135">Para permitir cualquier número de puerto, establezca " \* ".</span><span class="sxs-lookup"><span data-stu-id="60379-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60379-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60379-136">Return value</span></span>

<span data-ttu-id="60379-137">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="60379-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="60379-138">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="60379-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="60379-139">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="60379-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60379-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60379-140">Remarks</span></span>

<span data-ttu-id="60379-141">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="60379-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="60379-142">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="60379-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60379-143">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60379-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60379-144">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="60379-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60379-145">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60379-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60379-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60379-146">Requirements</span></span>



| <span data-ttu-id="60379-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="60379-147">Requirement</span></span> | <span data-ttu-id="60379-148">Value</span><span class="sxs-lookup"><span data-stu-id="60379-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60379-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60379-149">Minimum supported client</span></span><br/> | <span data-ttu-id="60379-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60379-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="60379-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60379-151">Minimum supported server</span></span><br/> | <span data-ttu-id="60379-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60379-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="60379-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60379-153">Namespace</span></span><br/>                | <span data-ttu-id="60379-154">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="60379-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="60379-155">MOF</span><span class="sxs-lookup"><span data-stu-id="60379-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60379-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60379-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="60379-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60379-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60379-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60379-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="60379-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="60379-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60379-160">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="60379-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

