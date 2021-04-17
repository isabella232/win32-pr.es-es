---
title: Método VerifyHealthMethod de la clase MDM_HealthAttestation
description: Método para notificar al dispositivo que prepare una solicitud de comprobación de certificado de mantenimiento. Vea también VerifyHealth.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Método VerifyHealthMethod
- Método VerifyHealthMethod, clase MDM_HealthAttestation
- Clase MDM_HealthAttestation, método VerifyHealthMethod
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656511"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="f7b2b-107">Método VerifyHealthMethod de la \_ clase HealthAttestation de MDM</span><span class="sxs-lookup"><span data-stu-id="f7b2b-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="f7b2b-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f7b2b-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7b2b-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f7b2b-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7b2b-110">Método para notificar al dispositivo que prepare una solicitud de comprobación de certificado de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="f7b2b-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="f7b2b-111">Vea también [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span><span class="sxs-lookup"><span data-stu-id="f7b2b-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b2b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7b2b-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="f7b2b-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7b2b-113">Parameters</span></span>

<span data-ttu-id="f7b2b-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f7b2b-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b2b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7b2b-115">Requirements</span></span>



| <span data-ttu-id="f7b2b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b2b-116">Requirement</span></span> | <span data-ttu-id="f7b2b-117">Value</span><span class="sxs-lookup"><span data-stu-id="f7b2b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b2b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7b2b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b2b-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b2b-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7b2b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7b2b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b2b-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f7b2b-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f7b2b-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f7b2b-122">Namespace</span></span><br/>                | <span data-ttu-id="f7b2b-123">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f7b2b-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f7b2b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="f7b2b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7b2b-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7b2b-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7b2b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7b2b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b2b-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b2b-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b2b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7b2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b2b-129">**HealthAttestation de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="f7b2b-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="f7b2b-130">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="f7b2b-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

