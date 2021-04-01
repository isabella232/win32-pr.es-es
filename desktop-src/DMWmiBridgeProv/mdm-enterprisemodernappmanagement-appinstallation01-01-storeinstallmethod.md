---
title: Método StoreInstallMethod de la clase MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Método para realizar una instalación de una aplicación y una licencia de la tienda Windows. Vea también StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Método StoreInstallMethod
- Método StoreInstallMethod, clase MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Clase MDM_EnterpriseModernAppManagement_AppInstallation01_01, método StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996789"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="858b1-107">Método StoreInstallMethod de la \_ clase EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="858b1-107">StoreInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="858b1-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="858b1-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="858b1-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="858b1-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="858b1-110">Método para realizar una instalación de una aplicación y una licencia de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="858b1-110">Method to perform an install of an app and a license from the Windows Store.</span></span> <span data-ttu-id="858b1-111">Vea también [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="858b1-111">See also, [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="858b1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="858b1-112">Syntax</span></span>


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="858b1-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="858b1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="858b1-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="858b1-114">*param* \[in\]</span></span>
<span data-ttu-id="858b1-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="858b1-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="858b1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="858b1-116">Requirements</span></span>



| <span data-ttu-id="858b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="858b1-117">Requirement</span></span> | <span data-ttu-id="858b1-118">Value</span><span class="sxs-lookup"><span data-stu-id="858b1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="858b1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="858b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="858b1-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="858b1-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="858b1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="858b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="858b1-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="858b1-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="858b1-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="858b1-123">Namespace</span></span><br/>                | <span data-ttu-id="858b1-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="858b1-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="858b1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="858b1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="858b1-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="858b1-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="858b1-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="858b1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="858b1-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="858b1-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="858b1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="858b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="858b1-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="858b1-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="858b1-131">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="858b1-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

