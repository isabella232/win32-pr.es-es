---
title: Método RemoveUserGroupNames de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad UserGroupNames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Método RemoveUserGroupNames Servicios de Escritorio remoto
- Método RemoveUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676752"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="b3d02-106">Método RemoveUserGroupNames de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="b3d02-106">RemoveUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="b3d02-107">Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="b3d02-107">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d02-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3d02-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="b3d02-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3d02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3d02-110">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3d02-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d02-111">Lista separada por puntos y comas de nombres de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3d02-111">Semicolon-separated list of user group names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3d02-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3d02-112">Return value</span></span>

<span data-ttu-id="b3d02-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b3d02-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b3d02-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b3d02-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b3d02-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b3d02-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d02-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3d02-116">Remarks</span></span>

<span data-ttu-id="b3d02-117">Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="b3d02-117">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="b3d02-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="b3d02-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b3d02-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b3d02-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3d02-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b3d02-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b3d02-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b3d02-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3d02-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b3d02-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d02-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d02-123">Requirements</span></span>



| <span data-ttu-id="b3d02-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d02-124">Requirement</span></span> | <span data-ttu-id="b3d02-125">Value</span><span class="sxs-lookup"><span data-stu-id="b3d02-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d02-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3d02-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d02-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b3d02-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b3d02-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3d02-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d02-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3d02-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b3d02-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3d02-130">Namespace</span></span><br/>                | <span data-ttu-id="b3d02-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b3d02-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b3d02-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b3d02-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3d02-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3d02-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3d02-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3d02-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3d02-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3d02-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b3d02-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3d02-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d02-137">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="b3d02-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

