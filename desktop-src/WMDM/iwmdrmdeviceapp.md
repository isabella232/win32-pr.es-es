---
title: IWMDRMDeviceApp (interfaz)
description: La interfaz IWMDRMDeviceApp permite a una aplicación medir, sincronizar licencias y actualizar los componentes DRM de un dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interfaz IWMDRMDeviceApp windows Media Administrador de dispositivos
- Interfaz IWMDRMDeviceApp windows Media Administrador de dispositivos , descrito
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d618a0534592ebe01a961ba9b0fdd462fcda70597b5f909b30e8fb92f6bdbeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055633"
---
# <a name="iwmdrmdeviceapp-interface"></a>IWMDRMDeviceApp (interfaz)

\[La Windows DRM de multimedia está en desuso y no debe usarse. Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) en su lugar.\]

La **interfaz IWMDRMDeviceApp** permite a una aplicación medir, sincronizar licencias y actualizar los componentes DRM de un dispositivo. Esta interfaz solo funcionará con dispositivos que admitan Windows DRM 10 multimedia para dispositivos portátiles.

Para obtener esta interfaz, llame a **CoCreateInstance** y pase CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Esta interfaz se define en el archivo de encabezado creado a partir de WMDRMDeviceApp.idl. Este encabezado **\# incluye**"wmdm.h". Es posible que tenga que cambiar este nombre de archivo para que coincida con el encabezado creado a partir de WMDM.idl.

 

## <a name="members"></a>Miembros

La **interfaz IWMDRMDeviceApp** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDeviceApp** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMDeviceApp** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Inicializa o restablece un reloj seguro del dispositivo.<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Adquiere datos de medición de un dispositivo.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Restablece algunos o todos los recuentos de medición de un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Consulta a un dispositivo su estado y funcionalidades actuales de DRM.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Actualiza las licencias de un dispositivo cuando están a punto de expirar.<br/>                                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> <dt>

[**Uso de contenido de medición**](metering-content-usage.md)
</dt> </dl>

 

