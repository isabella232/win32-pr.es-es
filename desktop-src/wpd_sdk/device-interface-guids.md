---
description: La interfaz del dispositivo se puede describir mediante un valor GUID. Dispositivos portátiles de Windows define la siguiente interfaz de dispositivo.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUID de interfaz de dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708930"
---
# <a name="device-interface-guids"></a><span data-ttu-id="7dbe2-104">GUID de interfaz de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7dbe2-104">Device Interface GUIDs</span></span>

<span data-ttu-id="7dbe2-105">La interfaz del dispositivo se puede describir mediante un valor **GUID** .</span><span class="sxs-lookup"><span data-stu-id="7dbe2-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="7dbe2-106">Dispositivos portátiles de Windows define la siguiente interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7dbe2-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="7dbe2-107">Constante</span><span class="sxs-lookup"><span data-stu-id="7dbe2-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="7dbe2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dbe2-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="7dbe2-109"><dt>**GUID \_ DEVINTERFACE \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="7dbe2-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="7dbe2-110">Identifica los dispositivos que aparecen en una enumeración de WPD normal.</span><span class="sxs-lookup"><span data-stu-id="7dbe2-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="7dbe2-111">Cualquier dispositivo que registre este GUID de interfaz se enumerará cuando una aplicación llame al método [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .</span><span class="sxs-lookup"><span data-stu-id="7dbe2-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="7dbe2-112"><dt>**GUID \_ DEVINTERFACE \_ WPD \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="7dbe2-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="7dbe2-113">Identifica los dispositivos que no aparecerán durante una enumeración de WPD normal.</span><span class="sxs-lookup"><span data-stu-id="7dbe2-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="7dbe2-114">Cualquier dispositivo que registre este GUID de interfaz se enumerará solo cuando una aplicación llame al método [**IPortableDeviceManager:: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .</span><span class="sxs-lookup"><span data-stu-id="7dbe2-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="7dbe2-115"><dt>**servicio de GUID \_ DEVINTERFACE \_ WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7dbe2-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="7dbe2-116">En Windows 7, las aplicaciones pueden enumerar todos los servicios de dispositivos de WPD llamando a [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) y usando esta clase de interfaz como el GUID del tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="7dbe2-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="7dbe2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dbe2-117">Requirements</span></span>



| <span data-ttu-id="7dbe2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dbe2-118">Requirement</span></span> | <span data-ttu-id="7dbe2-119">Value</span><span class="sxs-lookup"><span data-stu-id="7dbe2-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbe2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7dbe2-120">Header</span></span><br/> | <dl> <span data-ttu-id="7dbe2-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dbe2-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dbe2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dbe2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dbe2-123">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="7dbe2-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




