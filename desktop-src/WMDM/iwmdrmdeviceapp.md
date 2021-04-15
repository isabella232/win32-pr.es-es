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
# <a name="iwmdrmdeviceapp-interface"></a>Interfaz IWMDRMDeviceApp

\[La característica Windows Media DRM está en desuso y no debe usarse. En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

La interfaz **IWMDRMDeviceApp** permite a una aplicación medir, sincronizar licencias y actualizar los componentes de DRM de un dispositivo. Esta interfaz solo funcionará con dispositivos que admitan Windows Media DRM 10 para dispositivos portátiles.

Para obtener esta interfaz, llame a **CoCreateInstance**, pasando CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Esta interfaz se define en el archivo de encabezado generado a partir de WMDRMDeviceApp. idl. Este encabezado **\# incluye**"WMDM. h". Es posible que deba cambiar este nombre de archivo para que coincida con el encabezado generado a partir de WMDM. idl.

 

## <a name="members"></a>Miembros

La interfaz **IWMDRMDeviceApp** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDeviceApp** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMDeviceApp** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Inicializa o restablece el reloj seguro de un dispositivo<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Adquiere datos de disponibilidad de un dispositivo.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Restablece algunos o todos los recuentos de disponibilidad en un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Consulta a un dispositivo el estado y las capacidades de DRM actuales.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Actualiza las licencias en un dispositivo cuando están a la expiración.<br/>                                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> <dt>

[**Uso del contenido de disponibilidad**](metering-content-usage.md)
</dt> </dl>

 

