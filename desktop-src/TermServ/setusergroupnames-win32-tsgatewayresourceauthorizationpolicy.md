---
title: Método SetUserGroupNames de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Establece la propiedad UserGroupNames para la Directiva de autorización de recursos Escritorio remoto (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Método SetUserGroupNames Servicios de Escritorio remoto
- Método SetUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150489"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="bd5db-106">Método SetUserGroupNames de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="bd5db-106">SetUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="bd5db-107">Establece la propiedad **UserGroupNames** para la Directiva de autorización de recursos de escritorio remoto (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="bd5db-107">Sets the **UserGroupNames** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5db-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd5db-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="bd5db-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd5db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd5db-110">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd5db-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd5db-111">Lista separada por puntos y comas de nombres de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bd5db-111">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="bd5db-112">Los nombres tienen el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="bd5db-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="bd5db-113">Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso.</span><span class="sxs-lookup"><span data-stu-id="bd5db-113">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd5db-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd5db-114">Return value</span></span>

<span data-ttu-id="bd5db-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="bd5db-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bd5db-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bd5db-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bd5db-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bd5db-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd5db-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd5db-118">Remarks</span></span>

<span data-ttu-id="bd5db-119">Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="bd5db-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="bd5db-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="bd5db-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bd5db-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bd5db-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bd5db-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bd5db-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bd5db-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bd5db-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bd5db-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bd5db-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd5db-125">Requirements</span></span>



| <span data-ttu-id="bd5db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd5db-126">Requirement</span></span> | <span data-ttu-id="bd5db-127">Value</span><span class="sxs-lookup"><span data-stu-id="bd5db-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5db-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd5db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5db-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bd5db-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bd5db-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd5db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5db-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd5db-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bd5db-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd5db-132">Namespace</span></span><br/>                | <span data-ttu-id="bd5db-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bd5db-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bd5db-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bd5db-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd5db-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd5db-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd5db-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd5db-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd5db-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd5db-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bd5db-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd5db-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5db-139">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="bd5db-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

