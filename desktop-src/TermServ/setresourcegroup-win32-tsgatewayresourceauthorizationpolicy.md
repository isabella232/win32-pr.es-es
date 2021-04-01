---
title: Método SetResourceGroup de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Establece el tipo y el nombre del grupo de recursos.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Método SetResourceGroup Servicios de Escritorio remoto
- Método SetResourceGroup Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetResourceGroup
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905412"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="bb57f-106">Método SetResourceGroup de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="bb57f-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="bb57f-107">Establece el tipo y el nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb57f-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb57f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb57f-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="bb57f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb57f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb57f-110">*ResourceGroupName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb57f-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb57f-111">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb57f-111">Resource group name.</span></span> <span data-ttu-id="bb57f-112">Este valor reemplaza la propiedad **ResourceGroupName** existente.</span><span class="sxs-lookup"><span data-stu-id="bb57f-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="bb57f-113">*ResourceGroupType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb57f-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb57f-114">Identifica el tipo del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb57f-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="bb57f-115">Este valor reemplaza la propiedad **ResourceGroupType** existente.</span><span class="sxs-lookup"><span data-stu-id="bb57f-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="bb57f-116">RG</span><span class="sxs-lookup"><span data-stu-id="bb57f-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="bb57f-117">Un grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bb57f-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="bb57f-118">CG</span><span class="sxs-lookup"><span data-stu-id="bb57f-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="bb57f-119">Grupo de equipos, tal como se almacena en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="bb57f-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="bb57f-120">TODOS</span><span class="sxs-lookup"><span data-stu-id="bb57f-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="bb57f-121">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="bb57f-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb57f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb57f-122">Return value</span></span>

<span data-ttu-id="bb57f-123">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="bb57f-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bb57f-124">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bb57f-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bb57f-125">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bb57f-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bb57f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb57f-126">Remarks</span></span>

<span data-ttu-id="bb57f-127">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="bb57f-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bb57f-128">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bb57f-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bb57f-129">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bb57f-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bb57f-130">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb57f-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bb57f-131">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bb57f-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb57f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb57f-132">Requirements</span></span>



| <span data-ttu-id="bb57f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb57f-133">Requirement</span></span> | <span data-ttu-id="bb57f-134">Value</span><span class="sxs-lookup"><span data-stu-id="bb57f-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb57f-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb57f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bb57f-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bb57f-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bb57f-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb57f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bb57f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb57f-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bb57f-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb57f-139">Namespace</span></span><br/>                | <span data-ttu-id="bb57f-140">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bb57f-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bb57f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bb57f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb57f-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb57f-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb57f-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb57f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb57f-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb57f-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bb57f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb57f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb57f-146">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="bb57f-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

