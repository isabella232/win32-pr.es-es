---
description: La interfaz del dispositivo se puede describir mediante un valor GUID. Windows Dispositivos portátiles define la siguiente interfaz de dispositivo.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUID de interfaz de dispositivo (PortableDevice.h)
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
ms.openlocfilehash: 6f4bd170aeae46f738f5ce4a5a98bc694583a19fe3e7fa6eccc21c86fdc871d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657925"
---
# <a name="device-interface-guids"></a>GUID de interfaz de dispositivo

La interfaz del dispositivo se puede describir mediante un **valor GUID.** Windows Dispositivos portátiles define la siguiente interfaz de dispositivo.



| Constante                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD**</dt> </dl>                          | Identifica los dispositivos que aparecen en una enumeración DE WPD normal. Cualquier dispositivo que registre este GUID de interfaz se enumerará cuando una aplicación llame al método [**IPortableDeviceManager::GetDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ PRIVATE**</dt> </dl> | Identifica los dispositivos que no aparecerán durante una enumeración de WPD normal. Cualquier dispositivo que registre este GUID de interfaz solo se enumerará cuando una aplicación llame al método [**IPortableDeviceManager::GetPrivateDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices)<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**SERVICIO \_ GUID DEVINTERFACE \_ WPD \_**</dt> </dl> | En Windows 7, las aplicaciones pueden enumerar todos los servicios de dispositivo WPD llamando a [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) y usando esta clase de interfaz como GUID de tipo de servicio.<br/>                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 




