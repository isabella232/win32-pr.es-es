---
title: Método Create de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Crea una directiva de autorización de recursos de Escritorio remoto (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_TSGatewayResourceAuthorizationPolicy (clase)
- Win32_TSGatewayResourceAuthorizationPolicy Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422023"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="8752f-106">Método Create de la \_ clase Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="8752f-106">Create method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="8752f-107">Crea una directiva de autorización de recursos de Escritorio remoto (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="8752f-107">Creates a Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="8752f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8752f-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="8752f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8752f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8752f-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-111">Nombre de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="8752f-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-112">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-113">Descripción de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="8752f-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-114">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-115">Indica si se va a habilitar la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="8752f-115">Indicates whether the RD RAP is to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-116">*ResourceGroupType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-116">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-117">Tipo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8752f-117">Resource group type.</span></span>

<dt>

<span data-ttu-id="8752f-118">RG</span><span class="sxs-lookup"><span data-stu-id="8752f-118">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="8752f-119">Un grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8752f-119">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-120">CG</span><span class="sxs-lookup"><span data-stu-id="8752f-120">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="8752f-121">Grupo de equipos, tal como se almacena en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8752f-121">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-122">TODOS</span><span class="sxs-lookup"><span data-stu-id="8752f-122">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="8752f-123">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="8752f-123">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8752f-124">*ResourceGroupName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-124">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-125">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8752f-125">Resource group name.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-126">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-127">Lista separada por puntos y comas de nombres de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="8752f-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="8752f-128">Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso.</span><span class="sxs-lookup"><span data-stu-id="8752f-128">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="8752f-129">Los nombres de grupos de usuarios deben tener el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="8752f-129">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-130">*ProtocolNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-131">Lista separada por puntos y comas de nombres de protocolo que están habilitados para esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="8752f-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="8752f-132">Los nombres deben coincidir con el valor devuelto del método [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="8752f-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8752f-133">*PortNumbers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8752f-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8752f-134">Lista separada por puntos y comas de números de puerto que están habilitados para esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="8752f-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="8752f-135">Para permitir cualquier número de puerto, establezca " \* ".</span><span class="sxs-lookup"><span data-stu-id="8752f-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8752f-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8752f-136">Return value</span></span>

<span data-ttu-id="8752f-137">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8752f-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8752f-138">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8752f-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8752f-139">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8752f-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8752f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8752f-140">Remarks</span></span>

<span data-ttu-id="8752f-141">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="8752f-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8752f-142">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8752f-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8752f-143">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8752f-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8752f-144">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8752f-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8752f-145">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8752f-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8752f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8752f-146">Requirements</span></span>



| <span data-ttu-id="8752f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="8752f-147">Requirement</span></span> | <span data-ttu-id="8752f-148">Value</span><span class="sxs-lookup"><span data-stu-id="8752f-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8752f-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8752f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="8752f-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8752f-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8752f-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8752f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="8752f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8752f-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8752f-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8752f-153">Namespace</span></span><br/>                | <span data-ttu-id="8752f-154">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8752f-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8752f-155">MOF</span><span class="sxs-lookup"><span data-stu-id="8752f-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8752f-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8752f-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8752f-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8752f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8752f-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8752f-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8752f-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8752f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8752f-160">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="8752f-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

