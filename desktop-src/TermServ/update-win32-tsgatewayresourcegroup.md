---
title: Método Update de la clase Win32_TSGatewayResourceGroup
description: Actualiza el grupo de recursos.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Método Update Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Servicios de Escritorio remoto de clase Win32_TSGatewayResourceGroup, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a7b1610fc14aa522fa4d8b7caf03fccd7b37375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422363"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="4d1da-106">Método Update de la \_ clase Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d1da-106">Update method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="4d1da-107">Actualiza el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1da-107">Updates the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1da-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d1da-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="4d1da-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d1da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d1da-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4d1da-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1da-111">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1da-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="4d1da-112">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4d1da-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1da-113">Descripción del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1da-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="4d1da-114">*Recursos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4d1da-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1da-115">Lista de recursos separados por punto y coma en este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1da-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="4d1da-116">Un " \* " hace referencia a todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1da-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d1da-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d1da-117">Return value</span></span>

<span data-ttu-id="4d1da-118">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="4d1da-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4d1da-119">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4d1da-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4d1da-120">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4d1da-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d1da-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d1da-121">Remarks</span></span>

<span data-ttu-id="4d1da-122">Si hay varios recursos en el parámetro de *recursos* y no se puede procesar uno de los recursos, no se procesará ninguno de los recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1da-122">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="4d1da-123">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="4d1da-123">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4d1da-124">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d1da-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d1da-125">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4d1da-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d1da-126">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4d1da-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d1da-127">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4d1da-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d1da-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d1da-128">Requirements</span></span>



| <span data-ttu-id="4d1da-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d1da-129">Requirement</span></span> | <span data-ttu-id="4d1da-130">Value</span><span class="sxs-lookup"><span data-stu-id="4d1da-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1da-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d1da-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4d1da-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4d1da-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4d1da-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d1da-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4d1da-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d1da-134">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4d1da-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d1da-135">Namespace</span></span><br/>                | <span data-ttu-id="4d1da-136">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4d1da-136">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4d1da-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4d1da-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d1da-138"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d1da-138"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d1da-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d1da-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d1da-140"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d1da-140"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4d1da-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d1da-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1da-142">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="4d1da-142">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

