---
title: Método AddUserGroupNames de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Agrega la lista, separada por puntos y comas, de nombres de grupos de usuarios a los grupos de usuarios existentes en la propiedad UserGroupNames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Método AddUserGroupNames Servicios de Escritorio remoto
- Método AddUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c5c3fcb57c60ff2ca4c14d2e42ff0acdc84f0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996083"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="47dda-106">Método AddUserGroupNames de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="47dda-106">AddUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="47dda-107">Agrega la lista, separada por puntos y comas, de nombres de grupos de usuarios a los grupos de usuarios existentes en la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="47dda-107">Adds the specified semicolon-separated list of user group names to the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="47dda-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47dda-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="47dda-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47dda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47dda-110">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47dda-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47dda-111">Lista separada por puntos y comas de nombres de grupos de usuarios que se van a agregar a la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="47dda-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="47dda-112">Los nombres de grupos de usuarios deben tener el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="47dda-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47dda-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47dda-113">Return value</span></span>

<span data-ttu-id="47dda-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="47dda-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="47dda-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="47dda-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="47dda-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="47dda-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47dda-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47dda-117">Remarks</span></span>

<span data-ttu-id="47dda-118">Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="47dda-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="47dda-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="47dda-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="47dda-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="47dda-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="47dda-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="47dda-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="47dda-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="47dda-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="47dda-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="47dda-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="47dda-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47dda-124">Requirements</span></span>



| <span data-ttu-id="47dda-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="47dda-125">Requirement</span></span> | <span data-ttu-id="47dda-126">Value</span><span class="sxs-lookup"><span data-stu-id="47dda-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47dda-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47dda-127">Minimum supported client</span></span><br/> | <span data-ttu-id="47dda-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="47dda-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="47dda-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47dda-129">Minimum supported server</span></span><br/> | <span data-ttu-id="47dda-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47dda-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="47dda-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47dda-131">Namespace</span></span><br/>                | <span data-ttu-id="47dda-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="47dda-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="47dda-133">MOF</span><span class="sxs-lookup"><span data-stu-id="47dda-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47dda-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47dda-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="47dda-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47dda-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47dda-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47dda-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="47dda-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="47dda-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47dda-138">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="47dda-138">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

