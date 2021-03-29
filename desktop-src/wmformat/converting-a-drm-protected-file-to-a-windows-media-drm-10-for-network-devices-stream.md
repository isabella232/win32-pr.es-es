---
title: Convertir un archivo de DRM-Protected en un flujo de Windows Media DRM 10 para dispositivos de red
description: Convertir un archivo de DRM-Protected en un flujo de Windows Media DRM 10 para dispositivos de red
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK, convertir archivos protegidos con DRM
- SDK de Windows Media Format, archivos protegidos con DRM
- Advanced Systems Format (ASF), convertir archivos protegidos con DRM
- ASF (formato de sistemas avanzados), conversión de archivos protegidos con DRM
- Advanced Systems Format (ASF), archivos protegidos con DRM
- ASF (formato de sistemas avanzados), archivos protegidos con DRM
- Administración de derechos digitales (DRM), convertir archivos protegidos con DRM
- DRM (administración de derechos digitales), convertir archivos protegidos con DRM
- Administración de derechos digitales (DRM), archivos protegidos con DRM
- DRM (administración de derechos digitales), archivos protegidos con DRM
- Windows Media Format SDK, Windows Media DRM 10 para dispositivos de red
- Windows Media Format SDK, DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), Windows Media DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), Windows Media DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), DRM 10 para dispositivos de red
- Administración de derechos digitales (DRM), Windows Media DRM 10 para dispositivos de red
- DRM (administración de derechos digitales), Windows Media DRM 10 para dispositivos de red
- Administración de derechos digitales (DRM), DRM 10 para dispositivos de red
- DRM (administración de derechos digitales), DRM 10 para dispositivos de red
- Windows Media DRM 10 para dispositivos de red, conversión de archivos protegidos con DRM
- DRM 10 para dispositivos de red, conversión de archivos protegidos con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788841"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Convertir un archivo de DRM-Protected en un flujo de Windows Media DRM 10 para dispositivos de red

Una vez registrado y validado un dispositivo, puede empezar a procesar los mensajes de solicitud de licencia desde él. Los dispositivos envían los mensajes de solicitud de licencia cuando se necesita una acción de la aplicación. La única acción admitida actualmente es "Play", que es una solicitud de datos seguros para la reproducción.

Cuando reciba un mensaje de solicitud de licencia, debe realizar los siguientes pasos:

1.  Analice el mensaje de solicitud de licencia llamando al método [**IWMDRMMessageParser::P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) .
2.  Obtenga la interfaz [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) para el dispositivo llamando al método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , pasando el certificado y el número de serie obtenidos en el paso 1.
3.  Compruebe que el dispositivo está listo para recibir datos seguros:
    -   Llame a [**IWMRegisteredDevice:: IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) para comprobar que el dispositivo se ha aprobado. La aprobación siempre debe basarse en las preferencias del usuario.
    -   Llame a [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) para comprobar que el dispositivo se ha validado en las últimas 48 horas. Si el dispositivo no es válido, debe realizar la detección de proximidad. Para obtener más información, vea [realizar la detección de proximidad](performing-proximity-detection.md).
    -   Llame a [**IWMRegisteredDevice:: IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) para comprobar que el dispositivo se ha abierto. Si el dispositivo no está abierto, puede abrirlo llamando a [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). Solo puede tener 10 dispositivos abiertos en el equipo a la vez. Es posible que tenga que cerrar otro dispositivo antes de poder abrir el para el que está procesando la solicitud. Para cerrar un dispositivo, llame al método [**IWMRegisteredDevice:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) .
4.  Cree una instancia del objeto del transcifrador DRM mediante una llamada a la función [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) .
5.  Llame al método [**IWMDRMTranscryptor:: Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) para inicializar el transcifrador. Este método toma un puntero a la implementación de la interfaz [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) , que usa para enviar mensajes de estado. Este método también devuelve un mensaje de solicitud de licencia que se debe enviar al dispositivo antes de continuar.
6.  Cuando el método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de la aplicación recibe el \_ mensaje de estado del transcifrador WMT \_ , llame al método [**IWMDRMTranscryptor:: Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) para buscar la posición de inicio adecuada en el archivo. Para comenzar al principio del archivo, debe llamar a **Seek** con el tiempo 0.
7.  El transcifrador envía un \_ \_ mensaje de búsqueda de descifrado WMT cuando está listo para entregar datos del archivo en el nuevo tiempo de presentación. Realice llamadas repetidas al método [**IWMDRMTranscryptor:: Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) para obtener fragmentos convertidos de datos multimedia. Cada llamada es asincrónica y no se completa hasta que \_ se recibe un mensaje de lectura del TRANScifrado WMT \_ . Cuando reciba el mensaje, puede enviar los datos al dispositivo receptor.
8.  Cuando recibe un mensaje de \_ lectura del TRANScifrador WMT \_ con el parámetro *HR* establecido en \_ EOF de \_ transcifrador NS, se ha \_ leído todo el archivo. En este punto, llame al método [**IWMDRMTranscryptor:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) para cerrar el archivo y liberar recursos.
9.  Cuando \_ se recibe el mensaje de TRANScifrador WMT \_ , puede liberar la interfaz [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el protocolo DRM 10 de Windows Media para dispositivos de red**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




