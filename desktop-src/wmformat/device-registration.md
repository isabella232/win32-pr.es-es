---
title: Registro de dispositivos
description: Registro de dispositivos
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows SDK de formato multimedia, registro de dispositivos
- Windows SDK de formato multimedia, registro de dispositivos
- Formato de sistemas avanzados (ASF), registro de dispositivos
- ASF (formato de sistemas avanzados), registro de dispositivos
- Formato de sistemas avanzados (ASF), registro de dispositivos
- ASF (formato de sistemas avanzados), registro de dispositivos
- administración de derechos digitales (DRM), registro de dispositivos
- DRM (administración de derechos digitales), registro de dispositivos
- administración de derechos digitales (DRM), registro de dispositivos
- DRM (administración de derechos digitales), registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360226"
---
# <a name="device-registration"></a>Registro de dispositivos

El SDK Windows Media Format proporciona acceso a la base de datos de registro de dispositivos. Esta base de datos está protegida en el equipo cliente y se usa para registrar dispositivos que admiten Windows DRM 10 multimedia para dispositivos de red.

Cuando se agrega un dispositivo a una red a la que está conectado el equipo cliente, el dispositivo intenta ponerse en contacto con una aplicación de transmisor de Windows Media DRM 10 para dispositivos de red. Después de establecer las comunicaciones, el dispositivo envía un mensaje de solicitud de registro.

La aplicación debe realizar los pasos siguientes cuando recibe un mensaje de solicitud de registro:

1.  Analice el mensaje llamando al [**método IWMDRMMessageParser::P arseRegistrationReqMsg.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) Este método recupera el certificado de dispositivo y el número de serie del dispositivo, ambos necesarios para identificar el dispositivo.
2.  Llame al [**método IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) y pase el certificado y el número de serie del dispositivo recuperados en el paso 1. Si se encuentra el dispositivo, ya está registrado y puede omitir el paso siguiente.
3.  Llame al [**método IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) para agregar el dispositivo a la base de datos de registro de dispositivos.

Puede acceder a información sobre cualquier dispositivo de la base de datos de registro recuperando el objeto de dispositivo registrado asociado a él. Hay dos maneras de obtener un objeto de dispositivo registrado. Si tiene el certificado y el número de serie del dispositivo, puede llamar al método [**IWMDeviceRegistration::GetRegisteredDeviceByID.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) Si no tiene el certificado y el número de serie del dispositivo, puede enumerar todos los dispositivos de la base de datos llamando a [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguido de llamadas repetidas a [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) hasta que una llamada devuelva S \_ FALSE.

Para que la aplicación pueda enviar datos a un dispositivo, debe asegurarse de que el dispositivo está aprobado, validado y abierto.

La aprobación del dispositivo debe implicar la interacción con el usuario. Cuando un dispositivo envía un mensaje de registro, la aplicación puede pedir al usuario que decida si el dispositivo debe recibir los datos de ese usuario. A continuación, actualice la base de datos de registro de dispositivos mediante una llamada al método [**IWMRegisteredDevice::Approve,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) pasando **TRUE** o **FALSE** según corresponda.

La validación también se denomina detección de proximidad. Se trata de un proceso por el que los objetos DRM internos del SDK de formato multimedia de Windows determinan si el dispositivo está lo suficientemente "cerca" del equipo que ejecuta la aplicación para transmitir medios de forma segura. La proximidad viene determinada por el tiempo que se tarda en obtener una respuesta a un mensaje. Esta característica está pensada para evitar que usuarios no autorizados accedan a la red y obtengan los medios protegidos. Para obtener más información, vea [Realizar la detección de proximidad.](performing-proximity-detection.md)

Para abrir un dispositivo, llame a [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Uso de drm Windows multimedia 10 para el protocolo de dispositivos de red**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




