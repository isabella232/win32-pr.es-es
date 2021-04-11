---
title: Método GetLicenseFromStoreMethod de la clase MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Método para obtener una licencia del almacén. Vea también GetLicenseFromStore.
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- Método GetLicenseFromStoreMethod
- Método GetLicenseFromStoreMethod, clase MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Clase MDM_EnterpriseModernAppManagement_StoreLicenses02_01, método GetLicenseFromStoreMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150717"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="84b91-107">Método GetLicenseFromStoreMethod de la \_ clase EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="84b91-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="84b91-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="84b91-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="84b91-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="84b91-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="84b91-110">Método para obtener una licencia del almacén.</span><span class="sxs-lookup"><span data-stu-id="84b91-110">Method for getting a license from the store.</span></span> <span data-ttu-id="84b91-111">Vea también [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="84b91-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="84b91-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84b91-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="84b91-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84b91-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b91-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84b91-114">*param* \[in\]</span></span>
<span data-ttu-id="84b91-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84b91-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="84b91-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b91-116">Requirements</span></span>



| <span data-ttu-id="84b91-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b91-117">Requirement</span></span> | <span data-ttu-id="84b91-118">Value</span><span class="sxs-lookup"><span data-stu-id="84b91-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b91-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84b91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84b91-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="84b91-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84b91-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84b91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84b91-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="84b91-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="84b91-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84b91-123">Namespace</span></span><br/>                | <span data-ttu-id="84b91-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="84b91-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="84b91-125">MOF</span><span class="sxs-lookup"><span data-stu-id="84b91-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84b91-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84b91-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84b91-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84b91-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84b91-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84b91-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b91-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="84b91-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b91-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="84b91-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="84b91-131">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="84b91-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

