---
title: Método UpgradeEditionWithProductKeyMethod de la clase MDM_WindowsLicensing
description: Especifica una clave de producto para una actualización de edición de dispositivos de escritorio de Windows 10. Vea también UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Método UpgradeEditionWithProductKeyMethod
- Método UpgradeEditionWithProductKeyMethod, clase MDM_WindowsLicensing
- Clase MDM_WindowsLicensing, método UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491933"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="e2303-107">Método UpgradeEditionWithProductKeyMethod de la \_ clase WindowsLicensing de MDM</span><span class="sxs-lookup"><span data-stu-id="e2303-107">UpgradeEditionWithProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="e2303-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e2303-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e2303-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e2303-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e2303-110">Especifica una clave de producto para una actualización de edición de dispositivos de escritorio de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2303-110">Enters a product key for an edition upgrade of Windows 10 desktop devices.</span></span> <span data-ttu-id="e2303-111">Vea también [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="e2303-111">See also, [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2303-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2303-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="e2303-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2303-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2303-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2303-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2303-115">La clave de producto.</span><span class="sxs-lookup"><span data-stu-id="e2303-115">The product key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2303-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2303-116">Requirements</span></span>



| <span data-ttu-id="e2303-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2303-117">Requirement</span></span> | <span data-ttu-id="e2303-118">Value</span><span class="sxs-lookup"><span data-stu-id="e2303-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2303-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2303-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2303-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2303-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2303-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2303-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2303-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e2303-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e2303-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2303-123">Namespace</span></span><br/>                | <span data-ttu-id="e2303-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e2303-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e2303-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e2303-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2303-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2303-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2303-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2303-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2303-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2303-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2303-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2303-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2303-130">**WindowsLicensing de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="e2303-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="e2303-131">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="e2303-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

