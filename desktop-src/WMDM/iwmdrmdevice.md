---
title: IWMDRMDevice (interfaz)
description: Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona con fines de documentación completa. La interfaz IWMDRMDevice permite a un proveedor de contenido seguro comunicarse con dispositivos que usan Windows Media DRM 10 para dispositivos portátiles.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interfaz IWMDRMDispositivo windows Media Administrador de dispositivos
- Interfaz IWMDRMDispositivo windows Media Administrador de dispositivos , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967819"
---
# <a name="iwmdrmdevice-interface"></a>IWMDRMDevice (interfaz)

Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona con fines de documentación completa.

La **interfaz IWMDRMDevice** permite que un proveedor de contenido seguro se comunique con los dispositivos que usan Windows Drm multimedia 10 para dispositivos portátiles.

## <a name="members"></a>Members

La **interfaz IWMDRMDevice** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDevice también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMDevice** tiene estos métodos.



| Método                                                                  | Descripción                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Recupera el certificado de dispositivo.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Recupera el desafío de medición.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Recupera el reloj seguro.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera el desafío de reloj seguro.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Recupera la lista de sincronización de licencias.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina si el dispositivo admite Windows DRM 10 multimedia para dispositivos portátiles.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Establece la respuesta de licencia.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Establece la respuesta de medición.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Establece la respuesta del reloj seguro.<br/>                                                   |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces para proveedores de servicios**](interfaces-for-service-providers.md)
</dt> </dl>

 

