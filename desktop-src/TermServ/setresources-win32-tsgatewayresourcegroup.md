---
title: Método SetResources de la clase Win32_TSGatewayResourceGroup
description: Establece la propiedad Resources para este grupo de recursos.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Método SetResources Servicios de Escritorio remoto
- Método SetResources Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de clase Servicios de Escritorio remoto, método SetResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422121"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="19add-106">Método SetResources de la \_ clase TSGatewayResourceGroup de Win32</span><span class="sxs-lookup"><span data-stu-id="19add-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="19add-107">Establece la propiedad **Resources** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19add-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="19add-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19add-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="19add-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19add-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19add-110">*Recursos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="19add-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19add-111">Lista de recursos separados por punto y coma en este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19add-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="19add-112">Un " \* " hace referencia a todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="19add-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19add-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19add-113">Return value</span></span>

<span data-ttu-id="19add-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="19add-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="19add-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="19add-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="19add-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="19add-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19add-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19add-117">Remarks</span></span>

<span data-ttu-id="19add-118">Si hay varios recursos en el parámetro de *recursos* y no se puede procesar uno de los recursos, no se procesará ninguno de los recursos.</span><span class="sxs-lookup"><span data-stu-id="19add-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="19add-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="19add-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="19add-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="19add-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="19add-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="19add-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="19add-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="19add-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="19add-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="19add-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="19add-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19add-124">Requirements</span></span>



| <span data-ttu-id="19add-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="19add-125">Requirement</span></span> | <span data-ttu-id="19add-126">Value</span><span class="sxs-lookup"><span data-stu-id="19add-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19add-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19add-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19add-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="19add-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="19add-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19add-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19add-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19add-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="19add-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19add-131">Namespace</span></span><br/>                | <span data-ttu-id="19add-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="19add-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="19add-133">MOF</span><span class="sxs-lookup"><span data-stu-id="19add-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19add-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19add-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="19add-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19add-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19add-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19add-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="19add-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="19add-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19add-138">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="19add-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

