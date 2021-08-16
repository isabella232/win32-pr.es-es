---
title: Envío de datos de ASF a un punto de publicación
description: Envío de datos de ASF a un punto de publicación
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows SDK de formato multimedia, envío de datos de ASF
- Windows SDK de formato multimedia, puntos de publicación
- Formato de sistemas avanzados (ASF), envío de datos
- ASF (formato de sistemas avanzados), enviar datos
- Formato de sistemas avanzados (ASF), puntos de publicación
- ASF (formato de sistemas avanzados), puntos de publicación
- puntos de publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f70c1a49ea7ff6272d0eef9f1a51ff79ec216ed9af445c3078d59dd19841dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197544"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Envío de datos de ASF a un punto de publicación

Puede usar el SDK Windows Media Format para insertar datos de ASF en un punto de publicación en un servidor Windows Media. A continuación, el servidor difunde los datos desde ese punto de publicación. Este escenario es útil si va a capturar o volver a codificar contenido en un equipo y desea distribuir el contenido desde otro equipo (o varios equipos). También es útil si necesita mover contenido de un equipo dentro de un firewall a un servidor multimedia de Windows fuera del firewall, ya que la distribución de inserción usa el protocolo HTTP.

> [!Note]  
> Un *punto de publicación* actúa básicamente como un redirector. El cliente especifica el punto de publicación en la dirección URL (por ejemplo, mms://MyServer/MyPublishingPoint) y el servidor lo traduce en una solicitud de contenido.

 

Para insertar datos en el punto de publicación, adjunte el objeto receptor de inserción al objeto de escritor. El receptor de inserción se usa para abrir la conexión al servidor y administrar la sesión de inserción. El objeto de escritor controla todos los demás aspectos de la creación del archivo.

Lleve a cabo los siguiente pasos:

1.  Cree el objeto de escritor llamando a la [**función WMCreateWriter,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) que devuelve un [**puntero IWMWriter.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
2.  Cree el objeto receptor de inserción llamando a la [**función WMCreateWriterPushSink,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) que devuelve un [**puntero IWMWriterPushSink.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)
3.  Asocie el receptor de red al escritor mediante una llamada a [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) en el escritor, con un puntero a la interfaz **IWMWriterPushSink** del receptor de red.
4.  Conectar al servidor llamando a [**IWMWriterPushSink::Conectar**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Escriba la secuencia. Este paso implica establecer el perfil en el objeto de escritor, enviar ejemplos al escritor y, posiblemente, otras tareas. Para obtener más información, vea [Escribir archivos ASF.](writing-asf-files.md) Otras tareas pueden incluir la configuración de atributos de metadatos (como se describe en [Trabajar](working-with-metadata.md)con metadatos) o la configuración de DRM en directo en la secuencia (como se describe en Habilitación de la compatibilidad [con DRM).](enabling-drm-support.md) Estas tareas se realizan exactamente igual que para la escritura de archivos asf.
6.  Cuando haya terminado de escribir, llame a [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) en el escritor para desasociar el objeto receptor de inserción.
7.  Llame [**a IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) en el receptor de inserción para finalizar la sesión con el servidor.

Estos pasos se muestran en la aplicación de ejemplo WMVNetWrite.

> [!Note]  
> Si va a enviar un archivo de solo vídeo de velocidad de bits muy baja, es posible que no empiece a reproducirse en el punto de publicación durante varios segundos. Esto puede ocurrir en varios casos, por ejemplo, cuando un único paquete contiene muchos fotogramas de vídeo pequeños y no hay audio, o cuando hay un intervalo de tiempo largo entre el primer paquete y el segundo paquete en un archivo de solo vídeo de baja velocidad de bits. Para evitar este problema, inserte una secuencia de audio silenciosa en el archivo.

 

## <a name="authentication"></a>Autenticación

El objeto receptor de inserción controla automáticamente la autenticación en el servidor. Sin embargo, es posible que la aplicación tenga que proporcionar credenciales. Esto se realiza a través de la interfaz de devolución de llamada **IWMCredentialCallback,** como se muestra a continuación:

1.  Implemente [**la interfaz IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) [**e IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) en la aplicación.
2.  Consulte el objeto receptor de inserción para la [**interfaz IWMRegisterCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
3.  Llame [**a IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) con un puntero a la interfaz **IWMStatusCallback de la** aplicación.
4.  Si el receptor de inserción necesita obtener las credenciales de la aplicación, consulta el puntero **IWMStatusCallback** para la interfaz **IWMCredentialCallback** y llama a [**IWMCredentialCallback::AcquireCredentials.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials) Para obtener información sobre este método, vea [Autenticación](authentication.md).
5.  Cuando haya terminado, llame a [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) para dejar de recibir notificaciones de eventos del receptor de inserción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Envío de datos de ASF a través de una red**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> <dt>

[**Objeto receptor de inserción de escritor**](writer-push-sink-object.md)
</dt> </dl>

 

 




