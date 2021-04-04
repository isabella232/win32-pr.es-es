---
title: Envío de datos ASF a un punto de publicación
description: Envío de datos ASF a un punto de publicación
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- SDK de Windows Media Format, envío de datos ASF
- SDK de Windows Media Format, puntos de publicación
- Advanced Systems Format (ASF), enviar datos
- ASF (formato de sistemas avanzados), enviar datos
- Advanced Systems Format (ASF), puntos de publicación
- ASF (formato de sistemas avanzados), puntos de publicación
- puntos de publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789243"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Envío de datos ASF a un punto de publicación

Puede usar el SDK de Windows Media Format para enviar datos ASF a un punto de publicación en un servidor de Windows Media. A continuación, el servidor difunde los datos desde ese punto de publicación. Este escenario es útil si va a capturar o volver a codificar contenido en un equipo y desea distribuir el contenido desde otro equipo (o varios equipos). También es útil si necesita trasladar contenido de un equipo dentro de un Firewall a un servidor de Windows Media fuera del firewall, ya que la distribución de la extracción usa el protocolo HTTP.

> [!Note]  
> Un *punto de publicación* actúa esencialmente como un Redirector. El cliente especifica el punto de publicación en la dirección URL (por ejemplo, mms://MyServer/MyPublishingPoint) y el servidor lo traduce en una solicitud de contenido.

 

Para insertar datos en el punto de publicación, adjunte el objeto de receptor de extracción al objeto de escritor. El receptor de inserciones se utiliza para abrir la conexión al servidor y administrar la sesión de extracción. El objeto de escritor controla todos los demás aspectos de la creación del archivo.

Lleve a cabo los siguiente pasos:

1.  Cree el objeto de escritor mediante una llamada a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , que devuelve un puntero [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .
2.  Cree el objeto de receptor de envío mediante una llamada a la función [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , que devuelve un puntero [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .
3.  Asocie el receptor de red al escritor mediante una llamada a [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) en el escritor, con un puntero a la interfaz **IWMWriterPushSink** del receptor de la red.
4.  Conéctese al servidor mediante una llamada a [**IWMWriterPushSink:: Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Escriba la secuencia. Este paso implica establecer el perfil en el objeto de escritor, enviar ejemplos al escritor y, posiblemente, otras tareas. Para obtener más información, consulte [Writing ASF files](writing-asf-files.md). Las tareas adicionales pueden incluir la configuración de atributos de metadatos (como se describe en [trabajar con metadatos](working-with-metadata.md)) o el establecimiento de DRM de Live en la secuencia (como se describe en [habilitación](enabling-drm-support.md)de la compatibilidad con DRM). Estas tareas se realizan exactamente como son para la escritura de archivos ASF.
6.  Cuando haya terminado de escribir, llame a [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) en el escritor para desasociar el objeto de receptor de la extracción.
7.  Llame a [**IWMWriterPushSink:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) en el receptor de inserciones para finalizar la sesión con el servidor.

Estos pasos se ilustran en la aplicación de ejemplo WMVNetWrite.

> [!Note]  
> Si va a enviar un archivo de solo vídeo de velocidad de bits muy baja, es posible que no empiece a reproducirse en el punto de publicación durante varios segundos. Esto puede ocurrir en varios casos, por ejemplo, cuando un solo paquete contiene muchos fotogramas de vídeo pequeños y sin audio, o cuando hay un intervalo de tiempo largo entre el primer paquete y el segundo paquete en un archivo de solo vídeo de velocidad de bits. Para evitar este problema, inserte una secuencia de audio silenciosa en el archivo.

 

## <a name="authentication"></a>Autenticación

El objeto de receptor de inserciones controla automáticamente la autenticación en el servidor. Sin embargo, es posible que la aplicación tenga que proporcionar credenciales. Esto se hace a través de la interfaz de devolución de llamada **IWMCredentialCallback** , como se indica a continuación:

1.  Implemente la interfaz [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) y [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) en la aplicación.
2.  Consulte el objeto de receptor de la extracción para la interfaz [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .
3.  Llame a [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) con un puntero a la interfaz **IWMStatusCallback** de la aplicación.
4.  Si el receptor de inserciones necesita obtener las credenciales de la aplicación, consulta el puntero **IWMStatusCallback** de la interfaz **IWMCredentialCallback** y llama a [**IWMCredentialCallback:: AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials). Para obtener información sobre este método, vea [autenticación](authentication.md).
5.  Cuando haya terminado, llame a [**IWMRegisterCallback:: Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) para detener la obtención de notificaciones de eventos del receptor de inserciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Envío de datos ASF a través de una red**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> <dt>

[**Objeto de receptor de inserciones de escritor**](writer-push-sink-object.md)
</dt> </dl>

 

 




