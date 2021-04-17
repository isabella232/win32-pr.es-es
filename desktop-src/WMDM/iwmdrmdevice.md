---
title: Interfaz IWMDRMDevice
description: Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona con fines de documentación completa. La interfaz IWMDRMDevice permite a un proveedor de contenido seguro comunicarse con dispositivos que usan Windows Media DRM 10 para dispositivos portátiles.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interfaz IWMDRMDevice Administrador de dispositivos de Windows Media
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, se describe
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359087"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="da6df-105">Interfaz IWMDRMDevice</span><span class="sxs-lookup"><span data-stu-id="da6df-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="da6df-106">Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona con fines de documentación completa.</span><span class="sxs-lookup"><span data-stu-id="da6df-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="da6df-107">La interfaz **IWMDRMDevice** permite a un proveedor de contenido seguro comunicarse con dispositivos que usan Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="da6df-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="da6df-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="da6df-108">Members</span></span>

<span data-ttu-id="da6df-109">La interfaz **IWMDRMDevice** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="da6df-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="da6df-110">**IWMDRMDevice** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="da6df-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="da6df-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="da6df-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="da6df-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="da6df-112">Methods</span></span>

<span data-ttu-id="da6df-113">La interfaz **IWMDRMDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="da6df-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="da6df-114">Método</span><span class="sxs-lookup"><span data-stu-id="da6df-114">Method</span></span>                                                                  | <span data-ttu-id="da6df-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="da6df-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da6df-116">**CleanDataStore**</span><span class="sxs-lookup"><span data-stu-id="da6df-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="da6df-117">Inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da6df-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="da6df-118">**GetDeviceCertificate**</span><span class="sxs-lookup"><span data-stu-id="da6df-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="da6df-119">Recupera el certificado de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da6df-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="da6df-120">**GetMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="da6df-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="da6df-121">Recupera el desafío de medición.</span><span class="sxs-lookup"><span data-stu-id="da6df-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="da6df-122">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="da6df-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="da6df-123">Recupera el reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="da6df-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="da6df-124">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="da6df-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="da6df-125">Recupera el desafío de reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="da6df-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="da6df-126">**GetSyncList**</span><span class="sxs-lookup"><span data-stu-id="da6df-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="da6df-127">Recupera la lista de sincronización de licencias.</span><span class="sxs-lookup"><span data-stu-id="da6df-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="da6df-128">**IsWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="da6df-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="da6df-129">Determina si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="da6df-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="da6df-130">**SetLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="da6df-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="da6df-131">Establece la respuesta de la licencia.</span><span class="sxs-lookup"><span data-stu-id="da6df-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="da6df-132">**SetMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="da6df-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="da6df-133">Establece la respuesta de medición.</span><span class="sxs-lookup"><span data-stu-id="da6df-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="da6df-134">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="da6df-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="da6df-135">Establece la respuesta de reloj segura.</span><span class="sxs-lookup"><span data-stu-id="da6df-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="da6df-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="da6df-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da6df-137">**Interfaces para proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="da6df-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

