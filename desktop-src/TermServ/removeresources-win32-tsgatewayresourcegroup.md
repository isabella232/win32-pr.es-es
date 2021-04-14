---
title: Método RemoveResources de la clase Win32_TSGatewayResourceGroup
description: Quita recursos del grupo de recursos.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Método RemoveResources Servicios de Escritorio remoto
- Método RemoveResources Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de clase Servicios de Escritorio remoto, método RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422613"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="dbfac-106">Método RemoveResources de la \_ clase TSGatewayResourceGroup de Win32</span><span class="sxs-lookup"><span data-stu-id="dbfac-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="dbfac-107">Quita recursos del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dbfac-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbfac-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="dbfac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbfac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfac-110">*Recursos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dbfac-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfac-111">Lista separada por punto y coma de los recursos que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="dbfac-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbfac-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbfac-112">Return value</span></span>

<span data-ttu-id="dbfac-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="dbfac-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="dbfac-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="dbfac-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="dbfac-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dbfac-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbfac-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbfac-116">Remarks</span></span>

<span data-ttu-id="dbfac-117">Si hay varios recursos en el parámetro de *recursos* y no se puede procesar uno de los recursos, no se procesará ninguno de los recursos.</span><span class="sxs-lookup"><span data-stu-id="dbfac-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="dbfac-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="dbfac-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="dbfac-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dbfac-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dbfac-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dbfac-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dbfac-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="dbfac-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dbfac-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dbfac-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfac-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbfac-123">Requirements</span></span>



| <span data-ttu-id="dbfac-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfac-124">Requirement</span></span> | <span data-ttu-id="dbfac-125">Value</span><span class="sxs-lookup"><span data-stu-id="dbfac-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfac-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbfac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfac-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dbfac-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="dbfac-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbfac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfac-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbfac-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="dbfac-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dbfac-130">Namespace</span></span><br/>                | <span data-ttu-id="dbfac-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="dbfac-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="dbfac-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dbfac-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbfac-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbfac-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbfac-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbfac-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbfac-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbfac-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dbfac-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbfac-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfac-137">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="dbfac-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

