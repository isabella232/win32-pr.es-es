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
# <a name="iwmdrmdevice-interface"></a>Interfaz IWMDRMDevice

Esta interfaz no está pensada para ser implementada por un proveedor de servicios, pero se proporciona con fines de documentación completa.

La interfaz **IWMDRMDevice** permite a un proveedor de contenido seguro comunicarse con dispositivos que usan Windows Media DRM 10 para dispositivos portátiles.

## <a name="members"></a>Miembros

La interfaz **IWMDRMDevice** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDevice** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMDevice** tiene estos métodos.



| Método                                                                  | Descripción                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Recupera el certificado de dispositivo.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Recupera el desafío de medición.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Recupera el reloj seguro.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera el desafío de reloj seguro.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Recupera la lista de sincronización de licencias.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Establece la respuesta de la licencia.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Establece la respuesta de medición.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Establece la respuesta de reloj segura.<br/>                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para proveedores de servicios**](interfaces-for-service-providers.md)
</dt> </dl>

 

