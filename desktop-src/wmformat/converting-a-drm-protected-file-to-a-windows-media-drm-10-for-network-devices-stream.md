---
title: Convertir un archivo DRM-Protected en un Windows DRM 10 para dispositivos de red
description: Convertir un archivo DRM-Protected en un Windows DRM 10 para dispositivos de red
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows SDK de formato multimedia, conversión de archivos protegidos con DRM
- Windows SDK de formato multimedia, archivos protegidos con DRM
- Formato de sistemas avanzados (ASF), conversión de archivos protegidos con DRM
- ASF (formato de sistemas avanzados), conversión de archivos protegidos con DRM
- Formato de sistemas avanzados (ASF), archivos protegidos con DRM
- ASF (formato de sistemas avanzados), archivos protegidos con DRM
- administración de derechos digitales (DRM), conversión de archivos protegidos con DRM
- DRM (administración de derechos digitales), conversión de archivos protegidos con DRM
- administración de derechos digitales (DRM), archivos protegidos por DRM
- DRM (administración de derechos digitales), archivos protegidos por DRM
- Windows SDK de formato multimedia, Windows DRM multimedia 10 para dispositivos de red
- Windows SDK de formato multimedia, DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), Windows Media DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), Windows DRM multimedia 10 para dispositivos de red
- Formato de sistemas avanzados (ASF), DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), DRM 10 para dispositivos de red
- administración de derechos digitales (DRM), Windows DRM multimedia 10 para dispositivos de red
- DRM (administración de derechos digitales), Windows DRM multimedia 10 para dispositivos de red
- administración de derechos digitales (DRM),DRM 10 para dispositivos de red
- DRM (administración de derechos digitales),DRM 10 para dispositivos de red
- Windows DRM multimedia 10 para dispositivos de red, conversión de archivos protegidos con DRM
- DRM 10 para dispositivos de red, conversión de archivos protegidos con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe5aa16b13f41c0376da84237a846612b7ae6e730e630be6ec4a45ce48ff4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848916"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Convertir un archivo DRM-Protected en un Windows DRM 10 para dispositivos de red

Después de registrar y validar un dispositivo, puede empezar a procesar los mensajes de solicitud de licencia desde él. Los dispositivos envían mensajes de solicitud de licencia cuando se necesita una acción de la aplicación. La única acción admitida actualmente es "Play", que es una solicitud de datos seguros para la reproducción.

Cuando reciba un mensaje de solicitud de licencia, debe realizar los pasos siguientes:

1.  Analice el mensaje de solicitud de licencia llamando al [**método IWMDRMMessageParser::P arseLicenseRequestMsg.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg)
2.  Obtenga la [**interfaz IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) del dispositivo mediante una llamada al método [**IWMDeviceRegistration::GetRegisteredDeviceByID,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) pasando el certificado y el número de serie obtenidos en el paso 1.
3.  Compruebe que el dispositivo está listo para recibir datos seguros:
    -   Llame [**a IWMRegisteredDevice::IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) para comprobar que el dispositivo se ha aprobado. La aprobación siempre debe basarse en las preferencias del usuario.
    -   Llame [**a IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) para comprobar que el dispositivo se ha validado en las últimas 48 horas. Si el dispositivo no es válido, debe realizar la detección de proximidad. Para obtener más información, vea [Realizar la detección de proximidad.](performing-proximity-detection.md)
    -   Llame [**a IWMRegisteredDevice::IsOpened para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) comprobar que el dispositivo se ha abierto. Si el dispositivo no está abierto, puede abrirlo llamando a [**IWMRegisteredDevice::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open) Solo puede tener 10 dispositivos abiertos en el equipo a la vez. Es posible que tenga que cerrar otro dispositivo para poder abrir el para el que está procesando la solicitud. Para cerrar un dispositivo, llame al [**método IWMRegisteredDevice::Close.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close)
4.  Cree una instancia del objeto de transcryptor DRM llamando a la [**función WMCreateDRMTranscryptor.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)
5.  Llame al [**método IWMDRMTranscryptor::Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) para inicializar el transcryptor. Este método toma un puntero a la implementación de la [**interfaz IWMStatusCallback,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) que usa para entregar mensajes de estado. Este método también devuelve un mensaje de solicitud de licencia que se debe enviar al dispositivo antes de continuar.
6.  Cuando el método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de la aplicación recibe el mensaje de estado WMT TRANSCRYPTOR INIT, llame al método \_ \_ [**IWMDRMTranscryptor::Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) para buscar la posición de inicio adecuada en el archivo. Para empezar al principio del archivo, debe llamar a **Seek** con el tiempo 0.
7.  El transcryptor envía un mensaje \_ WMT TRANSCRYPTOR SEEKED cuando está listo para entregar datos del archivo en \_ el nuevo momento de presentación. Realice llamadas repetidas al [**método IWMDRMTranscryptor::Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) para obtener fragmentos convertidos de datos multimedia. Cada llamada es asincrónica y no se completa hasta que se recibe un mensaje \_ TRANSCRYPTOR \_ READ de WMT. Cuando reciba el mensaje, puede enviar los datos al dispositivo receptor.
8.  Cuando recibe un mensaje WMT TRANSCRYPTOR READ con el parámetro hr establecido en \_ \_ NS S  \_ \_ TRANSCRYPTOR \_ EOF, se ha leído todo el archivo. En este punto, llame al [**método IWMDRMTranscryptor::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) para cerrar el archivo y liberar recursos.
9.  Cuando se recibe el \_ mensaje WMT TRANSCRYPTOR CLOSED, puede liberar \_ la interfaz [**IWMDRMTranscryptor.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor)

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de Windows Drm 10 multimedia para el protocolo de dispositivos de red**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




