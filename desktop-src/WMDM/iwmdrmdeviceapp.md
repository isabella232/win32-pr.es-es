---
title: Interfaz IWMDRMDeviceApp
description: La interfaz IWMDRMDeviceApp permite a una aplicación medir, sincronizar licencias y actualizar los componentes de DRM de un dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interfaz IWMDRMDeviceApp Administrador de dispositivos de Windows Media
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, se describe
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695720"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="b3a7f-105">Interfaz IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="b3a7f-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="b3a7f-106">\[La característica Windows Media DRM está en desuso y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="b3a7f-107">En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="b3a7f-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="b3a7f-108">La interfaz **IWMDRMDeviceApp** permite a una aplicación medir, sincronizar licencias y actualizar los componentes de DRM de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="b3a7f-109">Esta interfaz solo funcionará con dispositivos que admitan Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="b3a7f-110">Para obtener esta interfaz, llame a **CoCreateInstance**, pasando CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="b3a7f-111">Esta interfaz se define en el archivo de encabezado generado a partir de WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="b3a7f-112">Este encabezado **\# incluye**"WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="b3a7f-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="b3a7f-113">Es posible que deba cambiar este nombre de archivo para que coincida con el encabezado generado a partir de WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="b3a7f-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3a7f-114">Members</span></span>

<span data-ttu-id="b3a7f-115">La interfaz **IWMDRMDeviceApp** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b3a7f-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b3a7f-116">**IWMDRMDeviceApp** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b3a7f-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="b3a7f-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="b3a7f-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b3a7f-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="b3a7f-118">Methods</span></span>

<span data-ttu-id="b3a7f-119">La interfaz **IWMDRMDeviceApp** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="b3a7f-120">Método</span><span class="sxs-lookup"><span data-stu-id="b3a7f-120">Method</span></span>                                                                   | <span data-ttu-id="b3a7f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a7f-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3a7f-122">**AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="b3a7f-123">Inicializa o restablece el reloj seguro de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="b3a7f-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="b3a7f-124">**GenerateMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="b3a7f-125">Adquiere datos de disponibilidad de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="b3a7f-126">**ProcessMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="b3a7f-127">Restablece algunos o todos los recuentos de disponibilidad en un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="b3a7f-128">**QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="b3a7f-129">Consulta a un dispositivo el estado y las capacidades de DRM actuales.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="b3a7f-130">**SynchronizeLicenses**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="b3a7f-131">Actualiza las licencias en un dispositivo cuando están a la expiración.</span><span class="sxs-lookup"><span data-stu-id="b3a7f-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="b3a7f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3a7f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a7f-133">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="b3a7f-134">**Interfaces para aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="b3a7f-135">**Uso del contenido de disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b3a7f-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

