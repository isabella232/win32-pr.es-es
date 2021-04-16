---
title: Método HostedInstallMethod de la clase MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Método para realizar una instalación de un paquete de la aplicación desde una ubicación hospedada, como una unidad local, un origen de datos UNC o HTTPS. Vea también HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Método HostedInstallMethod
- Método HostedInstallMethod, clase MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Clase MDM_EnterpriseModernAppManagement_AppInstallation01_01, método HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658278"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="d5e99-107">Método HostedInstallMethod de la \_ clase EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="d5e99-107">HostedInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="d5e99-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d5e99-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d5e99-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d5e99-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d5e99-110">Método para realizar una instalación de un paquete de la aplicación desde una ubicación hospedada, como una unidad local, un origen de datos UNC o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d5e99-110">Method to perform an install of an app package from a hosted location, such as a local drive, a UNC, or HTTPS data source.</span></span> <span data-ttu-id="d5e99-111">Vea también [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="d5e99-111">See also, [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e99-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5e99-112">Syntax</span></span>


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="d5e99-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5e99-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e99-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5e99-114">*param* \[in\]</span></span>
<span data-ttu-id="d5e99-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d5e99-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d5e99-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e99-116">Requirements</span></span>



| <span data-ttu-id="d5e99-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e99-117">Requirement</span></span> | <span data-ttu-id="d5e99-118">Value</span><span class="sxs-lookup"><span data-stu-id="d5e99-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e99-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e99-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5e99-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5e99-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e99-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5e99-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d5e99-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5e99-123">Namespace</span></span><br/>                | <span data-ttu-id="d5e99-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="d5e99-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d5e99-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d5e99-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5e99-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5e99-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5e99-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5e99-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5e99-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5e99-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e99-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5e99-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e99-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="d5e99-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="d5e99-131">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="d5e99-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

