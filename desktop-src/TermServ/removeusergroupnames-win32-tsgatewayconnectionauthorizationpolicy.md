---
title: Método RemoveUserGroupNames de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad UserGroupNames.
ms.assetid: 4ddbac15-7054-482a-8b5c-49551561673e
ms.tgt_platform: multiple
keywords:
- Método RemoveUserGroupNames Servicios de Escritorio remoto
- Método RemoveUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e4c3d9556243bcb28167378fea6018b4cd2ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996125"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="8b0fe-106">Método RemoveUserGroupNames de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="8b0fe-106">RemoveUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="8b0fe-107">Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="8b0fe-107">Removes specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0fe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b0fe-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="8b0fe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b0fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0fe-110">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b0fe-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0fe-111">Nombres de grupos de usuarios que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-111">User group names to remove.</span></span> <span data-ttu-id="8b0fe-112">Los nombres de grupos de usuarios deben tener el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0fe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b0fe-113">Return value</span></span>

<span data-ttu-id="8b0fe-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8b0fe-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8b0fe-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8b0fe-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b0fe-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b0fe-117">Remarks</span></span>

<span data-ttu-id="8b0fe-118">Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="8b0fe-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8b0fe-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8b0fe-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8b0fe-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8b0fe-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8b0fe-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8b0fe-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8b0fe-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0fe-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b0fe-124">Requirements</span></span>



| <span data-ttu-id="8b0fe-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b0fe-125">Requirement</span></span> | <span data-ttu-id="8b0fe-126">Value</span><span class="sxs-lookup"><span data-stu-id="8b0fe-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0fe-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b0fe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0fe-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8b0fe-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8b0fe-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b0fe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0fe-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b0fe-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8b0fe-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8b0fe-131">Namespace</span></span><br/>                | <span data-ttu-id="8b0fe-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8b0fe-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8b0fe-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0fe-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0fe-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b0fe-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0fe-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b0fe-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0fe-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b0fe-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8b0fe-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b0fe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0fe-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="8b0fe-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

