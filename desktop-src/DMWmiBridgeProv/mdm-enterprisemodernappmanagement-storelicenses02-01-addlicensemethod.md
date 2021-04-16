---
title: Método AddLicenseMethod de la clase MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Método para agregar la licencia. Vea también AddLicense.
ms.assetid: 325d284d-10ac-4786-8b04-8184ac43b53f
keywords:
- Método AddLicenseMethod
- Método AddLicenseMethod, clase MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Clase MDM_EnterpriseModernAppManagement_StoreLicenses02_01, método AddLicenseMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.AddLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f104f4e74d0200cc9d00b9f116232aa5308738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658273"
---
# <a name="addlicensemethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="7dfaa-107">Método AddLicenseMethod de la \_ clase EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="7dfaa-107">AddLicenseMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="7dfaa-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7dfaa-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7dfaa-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7dfaa-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7dfaa-110">Método para agregar la licencia.</span><span class="sxs-lookup"><span data-stu-id="7dfaa-110">Method for adding license.</span></span> <span data-ttu-id="7dfaa-111">Vea también [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="7dfaa-111">See also, [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7dfaa-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7dfaa-112">Syntax</span></span>


```mof
uint32 AddLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7dfaa-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dfaa-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dfaa-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7dfaa-114">*param* \[in\]</span></span>
<span data-ttu-id="7dfaa-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7dfaa-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7dfaa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dfaa-116">Requirements</span></span>



| <span data-ttu-id="7dfaa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dfaa-117">Requirement</span></span> | <span data-ttu-id="7dfaa-118">Value</span><span class="sxs-lookup"><span data-stu-id="7dfaa-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dfaa-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dfaa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7dfaa-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7dfaa-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7dfaa-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dfaa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7dfaa-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7dfaa-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7dfaa-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7dfaa-123">Namespace</span></span><br/>                | <span data-ttu-id="7dfaa-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7dfaa-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7dfaa-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7dfaa-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7dfaa-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7dfaa-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7dfaa-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7dfaa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dfaa-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dfaa-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dfaa-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dfaa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dfaa-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="7dfaa-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="7dfaa-131">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="7dfaa-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

