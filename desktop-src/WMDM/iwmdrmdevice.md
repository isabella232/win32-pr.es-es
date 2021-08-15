---
title: IWMDRMDevice (interfaz)
description: Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona para fines de documentación completa. La interfaz IWMDRMDevice permite a un proveedor de contenido seguro comunicarse con dispositivos que usan Windows Media DRM 10 para dispositivos portátiles.
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
ms.openlocfilehash: fee40eb6fdada2374b0f571a201ff53fb38f41de7f3cac5eeaa2159475bfdb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005125"
---
# <a name="iwmdrmdevice-interface"></a>IWMDRMDevice (interfaz)

Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona para fines de documentación completa.

La **interfaz IWMDRMDevice** permite que un proveedor de contenido seguro se comunique con dispositivos que usan Windows Media DRM 10 para dispositivos portátiles.

## <a name="members"></a>Miembros

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
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera el desafío del reloj seguro.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Recupera la lista de sincronización de licencias.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina si el dispositivo admite drm Windows multimedia 10 para dispositivos portátiles.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Establece la respuesta de la licencia.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Establece la respuesta de medición.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Establece la respuesta del reloj seguro.<br/>                                                   |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces para proveedores de servicios**](interfaces-for-service-providers.md)
</dt> </dl>

 

