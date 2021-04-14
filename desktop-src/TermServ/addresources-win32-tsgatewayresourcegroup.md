---
title: Método AddResources de la clase Win32_TSGatewayResourceGroup
description: Agrega recursos al grupo de recursos.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Método AddResources Servicios de Escritorio remoto
- Método AddResources Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de clase Servicios de Escritorio remoto, método AddResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533849"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="45e0d-106">Método AddResources de la \_ clase TSGatewayResourceGroup de Win32</span><span class="sxs-lookup"><span data-stu-id="45e0d-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="45e0d-107">Agrega recursos al grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45e0d-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="45e0d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45e0d-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="45e0d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45e0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45e0d-110">*Recursos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="45e0d-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e0d-111">Lista separada por puntos y comas de los recursos que se van a agregar al grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45e0d-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="45e0d-112">Un " \* " hace referencia a todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="45e0d-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45e0d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45e0d-113">Return value</span></span>

<span data-ttu-id="45e0d-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="45e0d-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="45e0d-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="45e0d-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="45e0d-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="45e0d-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45e0d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45e0d-117">Remarks</span></span>

<span data-ttu-id="45e0d-118">Si hay varios recursos en el parámetro de *recursos* y no se puede procesar uno de los recursos, no se procesará ninguno de los recursos.</span><span class="sxs-lookup"><span data-stu-id="45e0d-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="45e0d-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="45e0d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="45e0d-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="45e0d-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="45e0d-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="45e0d-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="45e0d-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="45e0d-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="45e0d-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="45e0d-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="45e0d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45e0d-124">Requirements</span></span>



| <span data-ttu-id="45e0d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45e0d-125">Requirement</span></span> | <span data-ttu-id="45e0d-126">Value</span><span class="sxs-lookup"><span data-stu-id="45e0d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e0d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45e0d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45e0d-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="45e0d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="45e0d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45e0d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45e0d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45e0d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="45e0d-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="45e0d-131">Namespace</span></span><br/>                | <span data-ttu-id="45e0d-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="45e0d-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="45e0d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="45e0d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45e0d-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45e0d-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="45e0d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45e0d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45e0d-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45e0d-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="45e0d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="45e0d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45e0d-138">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="45e0d-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

