---
title: Método EnrollMethod de la clase MDM_ClientCertificateInstall_Install03
description: Desencadena el dispositivo para iniciar la inscripción de certificados.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Método EnrollMethod
- Método EnrollMethod, clase MDM_ClientCertificateInstall_Install03
- Clase MDM_ClientCertificateInstall_Install03, método EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803128"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="199d6-106">Método EnrollMethod de la \_ \_ clase INSTALL03 de MDM ClientCertificateInstall</span><span class="sxs-lookup"><span data-stu-id="199d6-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="199d6-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="199d6-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="199d6-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="199d6-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="199d6-109">Desencadena el dispositivo para iniciar la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="199d6-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="199d6-110">El dispositivo no notificará al servidor MDM una vez que se haya realizado la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="199d6-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="199d6-111">El servidor MDM podría consultar posteriormente el dispositivo para averiguar si se ha agregado el nuevo certificado.</span><span class="sxs-lookup"><span data-stu-id="199d6-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="199d6-112">Vea también [**inscribir**](/windows/client-management/mdm/clientcertificateinstall-csp).</span><span class="sxs-lookup"><span data-stu-id="199d6-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="199d6-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="199d6-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="199d6-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="199d6-114">Parameters</span></span>

<span data-ttu-id="199d6-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="199d6-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="199d6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="199d6-116">Return value</span></span>

<span data-ttu-id="199d6-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="199d6-117">Required.</span></span> <span data-ttu-id="199d6-118">Desencadena el dispositivo para iniciar la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="199d6-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="199d6-119">El dispositivo no notificará al servidor MDM una vez que se haya realizado la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="199d6-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="199d6-120">El servidor MDM podría consultar posteriormente el dispositivo para averiguar si se ha agregado el nuevo certificado.</span><span class="sxs-lookup"><span data-stu-id="199d6-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="199d6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="199d6-121">Requirements</span></span>



| <span data-ttu-id="199d6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="199d6-122">Requirement</span></span> | <span data-ttu-id="199d6-123">Value</span><span class="sxs-lookup"><span data-stu-id="199d6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="199d6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="199d6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="199d6-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="199d6-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="199d6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="199d6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="199d6-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="199d6-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="199d6-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="199d6-128">Namespace</span></span><br/>                | <span data-ttu-id="199d6-129">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="199d6-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="199d6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="199d6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="199d6-131"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="199d6-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="199d6-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="199d6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="199d6-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="199d6-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="199d6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="199d6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199d6-135">**\_Install03 CLIENTCERTIFICATEINSTALL \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="199d6-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="199d6-136">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="199d6-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

