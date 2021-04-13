---
title: Método AddUserGroupNames de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Agrega los nombres de grupos de usuarios especificados a la propiedad UserGroupNames.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- Método AddUserGroupNames Servicios de Escritorio remoto
- Método AddUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a4fe26b27f954e5ea9a0c7ac666592f74337a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422092"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="83263-106">Método AddUserGroupNames de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="83263-106">AddUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="83263-107">Agrega los nombres de grupos de usuarios especificados a la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="83263-107">Adds the specified user group names to the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="83263-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83263-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="83263-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83263-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83263-110">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83263-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83263-111">Lista separada por puntos y comas de nombres de grupos de usuarios que se van a agregar a la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="83263-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="83263-112">Los nombres de grupos de usuarios deben tener el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="83263-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83263-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83263-113">Return value</span></span>

<span data-ttu-id="83263-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="83263-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="83263-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="83263-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="83263-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="83263-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="83263-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83263-117">Remarks</span></span>

<span data-ttu-id="83263-118">Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="83263-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="83263-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="83263-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="83263-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="83263-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="83263-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="83263-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="83263-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="83263-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="83263-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="83263-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="83263-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83263-124">Requirements</span></span>



| <span data-ttu-id="83263-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="83263-125">Requirement</span></span> | <span data-ttu-id="83263-126">Value</span><span class="sxs-lookup"><span data-stu-id="83263-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83263-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83263-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83263-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="83263-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="83263-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83263-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83263-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83263-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="83263-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83263-131">Namespace</span></span><br/>                | <span data-ttu-id="83263-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="83263-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="83263-133">MOF</span><span class="sxs-lookup"><span data-stu-id="83263-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83263-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83263-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="83263-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83263-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83263-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83263-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="83263-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="83263-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83263-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="83263-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

