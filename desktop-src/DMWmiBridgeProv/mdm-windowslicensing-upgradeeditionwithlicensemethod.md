---
title: Método UpgradeEditionWithLicenseMethod de la clase MDM_WindowsLicensing
description: Método para proporcionar una licencia para una actualización de edición de dispositivos Windows 10 Mobile. Vea también UpgradeEditionWithLicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Método UpgradeEditionWithLicenseMethod
- Método UpgradeEditionWithLicenseMethod, clase MDM_WindowsLicensing
- Clase MDM_WindowsLicensing, método UpgradeEditionWithLicenseMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996779"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="46eac-107">Método UpgradeEditionWithLicenseMethod de la \_ clase WindowsLicensing de MDM</span><span class="sxs-lookup"><span data-stu-id="46eac-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="46eac-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="46eac-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="46eac-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="46eac-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="46eac-110">Método para proporcionar una licencia para una actualización de edición de dispositivos Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="46eac-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="46eac-111">Vea también [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="46eac-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="46eac-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46eac-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="46eac-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46eac-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46eac-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46eac-114">*param* \[in\]</span></span>
<span data-ttu-id="46eac-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46eac-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="46eac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46eac-116">Requirements</span></span>



| <span data-ttu-id="46eac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46eac-117">Requirement</span></span> | <span data-ttu-id="46eac-118">Value</span><span class="sxs-lookup"><span data-stu-id="46eac-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46eac-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46eac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46eac-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="46eac-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46eac-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46eac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46eac-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="46eac-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="46eac-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46eac-123">Namespace</span></span><br/>                | <span data-ttu-id="46eac-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="46eac-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="46eac-125">MOF</span><span class="sxs-lookup"><span data-stu-id="46eac-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46eac-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46eac-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="46eac-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46eac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46eac-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46eac-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46eac-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="46eac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46eac-130">**WindowsLicensing de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="46eac-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="46eac-131">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="46eac-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

