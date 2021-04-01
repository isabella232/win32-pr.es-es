---
title: Método CheckApplicabilityMethod de la clase MDM_WindowsLicensing
description: Comprueba si se puede usar la clave de producto especificada para una actualización de edición, activación o cambio de una clave de producto de Windows 10 para dispositivos de escritorio. Vea también CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Método CheckApplicabilityMethod
- Método CheckApplicabilityMethod, clase MDM_WindowsLicensing
- Clase MDM_WindowsLicensing, método CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150706"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="8701f-107">Método CheckApplicabilityMethod de la \_ clase WindowsLicensing de MDM</span><span class="sxs-lookup"><span data-stu-id="8701f-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="8701f-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="8701f-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8701f-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="8701f-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8701f-110">Comprueba si se puede usar la clave de producto especificada para una actualización de edición, activación o cambio de una clave de producto de Windows 10 para dispositivos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="8701f-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="8701f-111">Vea también [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="8701f-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="8701f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8701f-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="8701f-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8701f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8701f-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8701f-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8701f-115">La clave de producto.</span><span class="sxs-lookup"><span data-stu-id="8701f-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8701f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8701f-116">Return value</span></span>

<span data-ttu-id="8701f-117">TRUE o FALSE</span><span class="sxs-lookup"><span data-stu-id="8701f-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="8701f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8701f-118">Requirements</span></span>



| <span data-ttu-id="8701f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8701f-119">Requirement</span></span> | <span data-ttu-id="8701f-120">Value</span><span class="sxs-lookup"><span data-stu-id="8701f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8701f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8701f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8701f-122">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8701f-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8701f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8701f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8701f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8701f-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8701f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8701f-125">Namespace</span></span><br/>                | <span data-ttu-id="8701f-126">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="8701f-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8701f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="8701f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8701f-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8701f-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8701f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8701f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8701f-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8701f-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8701f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8701f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8701f-132">**WindowsLicensing de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="8701f-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="8701f-133">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="8701f-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

