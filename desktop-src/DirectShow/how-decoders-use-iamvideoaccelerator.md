---
description: Cómo usan los descodificadores IAMVideoAccelerator
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Cómo usan los descodificadores IAMVideoAccelerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169926"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Cómo usan los descodificadores IAMVideoAccelerator

La [**interfaz IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) permite operaciones genéricas de aceleración de vídeo, incluida la aceleración de vídeo directX (VA). Para la aceleración de VA que no es de DirectX, el descodificador y el controlador de vídeo deben cumplir un protocolo común.

En esta sección se describe el orden general de las operaciones que debe seguir cualquier descodificador al usar esta interfaz. Puede encontrar más información específica sobre los descodificadores basados en VA de DirectX en [Mapping DirectX Video Acceleration to IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md)(Asignación de aceleración de vídeo DirectX a IAMVideoAccelerator).

> [!Note]  
> Esta interfaz está disponible en Windows 2000 y versiones posteriores.

 

La [**interfaz IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) se expone en el pin de entrada de [overlay Mixer](overlay-mixer-filter.md) o video mixing Renderer (VMR). La [**interfaz IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) se expone en el pin de salida del descodificador. La secuencia de eventos para conectar los pines de filtro es la siguiente:

1.  El Administrador Graph filtros llama a [**IPin::Conectar**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) en el pin de salida del filtro del descodificador. Am [**\_ MEDIA TYPE \_ es**](/windows/win32/api/strmif/ns-strmif-am_media_type) un parámetro opcional.
    -   [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) es una estructura de datos que describe un tipo de medio. Contiene un GUID de tipo principal (que en nuestro caso debe ser VÍDEO DE MEDIATYPE), un GUID de subtipo (que en nuestro caso debe ser un GUID del acelerador de vídeo) y otras \_ muchas cosas. Una de esas cosas es un GUID de tipo de formato que contiene información sobre los medios, incluido en nuestro caso el ancho y alto de una imagen de vídeo sin comprimir, probablemente en una estructura [**MPEG1VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)o [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)
    -   La [**estructura AM MEDIA \_ \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) si está presente, indica al descodificador que funcione con el tipo de medio especificado, que puede ser "totalmente especificado" o "parcialmente especificado". Si es "totalmente especificado", el descodificador normalmente simplemente intentaría funcionar con ese tipo de medio. Si "se especifica parcialmente", intentará encontrar un modo de operación compatible "totalmente especificado" que pueda usar para conectarse de forma coherente con el tipo de medio "parcialmente especificado".
    -   La manera normal de intentar encontrar un tipo de medio "totalmente especificado" que se va a usar para una conexión es simplemente ejecutar una lista de todos los tipos de medios "totalmente especificados" que admite el pin de salida, que es compatible con el tipo de medio "parcialmente especificado" e intentar conectarse con cada uno de ellos hasta que se haya realizado correctamente. Normalmente, el proceso sería similar si no hay ningún TIPO DE MEDIO DE AM incluido en la llamada \_ \_ a [**IPin::Conectar,**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) pero con el pin de salida que necesita comprobar todos sus tipos de medios.
2.  Si el descodificador desea comprobar si el pin de entrada de nivel inferior admite un TIPO MULTIMEDIA de AM específico (incluido un GUID del acelerador de vídeo), puede llamar al [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) de ese pin (con el GUID del acelerador de vídeo como subtipo de AM **MEDIA \_ \_ TYPE)** o simplemente intentar conectarse a ese pin como se describe en el elemento 5 a continuación. [**\_ \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)
3.  Si el descodificador no sabe qué GUID del acelerador de vídeo admite el pin de entrada de bajada y no desea proponer solo algún GUID de acelerador de vídeo candidato concreto mediante una llamada a [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)del pin de entrada de bajada, el descodificador puede llamar a [**IAMVideoAccelerator::GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) para obtener una lista de los GUID del acelerador de vídeo que admite el pin.
4.  Para algunos GUID de acelerador de vídeo concretos, el descodificador puede llamar al [**elemento IAMVideoAccelerator::GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) del pin de entrada de bajada para obtener una lista de los formatos de **píxeles DDPIXELFORMAT** que se pueden usar para representar un GUID específico del acelerador de vídeo. La lista devuelta debe considerarse en orden de preferencias decreciente (es decir, con el formato más preferido enumerado primero).
5.  El descodificador llama al [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)del pin de entrada de bajada y le pasa un AM [**\_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) con el GUID del acelerador de vídeo adecuado como subtipo del tipo de medio. Esto configura la conexión para la operación, incluida la creación de las superficies de salida sin comprimir (que se asignan con el ancho y alto encontrados en **AM \_ MEDIA \_ TYPE,** y el número de superficies que se van a asignar encontradas mediante una llamada descrita a continuación, y cualquier otra información que el acelerador de vídeo tenga disponible y desee usar para ese propósito, como el propio GUID del acelerador de vídeo). Si el pin de entrada de bajada rechaza el GUID del acelerador de vídeo o algún otro aspecto de la conexión, esto puede provocar un error en **IPin::ReceiveConnection.** Si se produce un error **en IPin::ReceiveConnection,** esto se indica en un **HRESULT** devuelto y el descodificador puede intentar realizar la llamada de nuevo, por ejemplo, con un nuevo GUID del acelerador de vídeo en la estructura **AM MEDIA \_ \_ TYPE.**
    -   [!Note]  
        > Esta es otra manera (y la más definitiva) para que el descodificador determine qué es compatible con el pin de entrada de bajada: simplemente llamando a [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e intentando conectarse y, a continuación, comprobando si el intento de conexión se ha realizado correctamente.

         

    -   Durante [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection), el representador llama a [**IAMVideoAcceleratorNotify::GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)del descodificador y le pasa el GUID del acelerador de vídeo y una estructura [**AMVAUncompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) para averiguar cuántas superficies sin comprimir asignar. El descodificador rellena y devuelve la estructura , que contiene el número mínimo y máximo de superficies que se asignarán del tipo determinado, y una estructura **DDPIXELFORMAT** que describe el formato de píxel de las superficies que se asignarán.
    -   [!Note]  
        > En realidad, no se pasa nada al descodificador en la llamada a [**IAMVideoAcceleratorNotify::GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) que no sea el GUID del acelerador de vídeo.

         

6.  El representador llama al [**elemento IAMVideoAcceleratorNotify::SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)del descodificador, pasando al descodificador el número real de superficies sin comprimir que se asignaron.
7.  El representador llama al [**elemento IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) del descodificador para obtener los datos necesarios para inicializar el acelerador de vídeo.
8.  El descodificador llama a [**IAMVideoAccelerator::GetCompBufferInfo,**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo)pasando un GUID del acelerador de vídeo, una estructura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) y el número de tipos de búfer comprimidos, para obtener un conjunto de estructuras de datos [**AMVACompBufferInfo,**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) una correspondiente a cada tipo de búfer de datos comprimido usado por el GUID del acelerador de vídeo.
    -   La [**estructura AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) contiene el ancho y alto de los datos sin comprimir descodificados (en píxeles) y el DDPIXELFORMAT de la imagen sin comprimir.
    -   Las [**estructuras de datos AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) devueltas contienen:
        -   Número de búferes comprimidos necesarios del tipo específico.
        -   Ancho y alto de la superficie que se va a crear (campos que pueden o no tener ningún significado real).
            > [!Note]  
            > La operación de asignación de superficies de DirectDraw para los búferes comprimidos no proporciona actualmente que el ancho o alto de estas superficies sea mayor o igual que 2^15, aunque es posible que la llamada de asignación de superficie no presente un error total si se infringe este límite. Por lo tanto, el controlador podría estructurar sus solicitudes de memoria de búfer comprimida para evitar estos tamaños extremos. Por ejemplo, en lugar de solicitar un búfer con width="1" y height="65536", el controlador debe solicitar un búfer de width="1024" y height="64".

             

        -   Número total de bytes que va a usar la superficie.
        -   Estructura de tipo **DDSCAPS2** que define un objeto DirectDrawSurface, que describe las funcionalidades para crear superficies para almacenar datos comprimidos.
        -   DDPIXELFORMAT, que describe el formato de píxel usado para crear superficies para almacenar datos comprimidos (un campo que puede o no tener ningún significado real).

> [!Note]  
> Las llamadas del representador a algunos de los métodos de interfaz [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) del descodificador pueden producirse (y normalmente lo harían) dentro de la llamada del descodificador al [**IPin::ReceiveConnection del representador.**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) En concreto, esto se aplica a lo siguiente:
>
> -   [**IAMVideoAcceleratorNotify::GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**IAMVideoAcceleratorNotify::SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo), y
> -   [**IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Para admitir cambios de formato dinámico, el descodificador también puede llamar a [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) y a otros métodos anteriores mientras los filtros están conectados y en ejecución. Esta funcionalidad se proporciona para admitir cambios de formato dinámico (aunque no en el sentido H.263, Anexo P, ya que todos los conjuntos de datos se inician de nuevo desde cero y, por tanto, se pierde cualquier información de imagen de referencia).

 

A continuación se muestra una descripción del uso de [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) durante la operación después de la inicialización:

1.  Para cada superficie sin comprimir, el descodificador llama a [**IAMVideoAccelerator::BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) para comenzar el procesamiento para crear la imagen de salida. Cuando lo hace, el descodificador envía una [**estructura AMVABeginFrameInfo.**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo)
    -   La estructura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) contiene un índice para un búfer de destino, un puntero a algunos datos que se envían de bajada y un puntero a un lugar donde el acelerador puede colocar algunos datos para que el descodificador lea.
    -   NOTA 1: El acelerador no recibe realmente el índice de búfer de destino, ya que el representador lo traduce antes de bajar.
    -   NOTA 2: Se puede llamar a [**IAMVideoAccelerator::BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) más de una vez entre llamadas a [**IAMVideoAccelerator::EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe).
    -   NOTA 3: No hay ninguna suposición dentro de la operación de interfaz de que es necesario llamar a [**IAMVideoAccelerator::BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) y [**IAMVideoAccelerator::EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) para el procesamiento de cada imagen individual del flujo de bits.

        Lo [**que hace IAMVideoAccelerator::BeginFrame,**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) en lo que respecta a la interfaz, es crear una asociación dentro del representador entre un índice y una superficie sin comprimir. También proporciona un medio para llamar a una función específica en un controlador de dispositivo (con compatibilidad con un medio de pasar datos arbitrarios entre el descodificador y el controlador del dispositivo).

        (Sin embargo, en la operación va de DirectX hay un requisito descrito a continuación que [**IAMVideoAccelerator::BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) y [**IAMVideoAccelerator::EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) deben llamarse para el procesamiento de cada imagen individual en la secuencia de bits).

2.  Para enviar datos sin comprimir al acelerador, el descodificador llama a:
    -   [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) para determinar si un búfer es seguro para leer o escribir en .
    -   [**IAMVideoAccelerator::GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) para bloquear y obtener acceso a un búfer especificado (si no lo ha llamado previamente para obtener ese acceso). **GetBuffer** también se puede usar para obtener una copia del contenido de la última imagen de salida sin comprimir para la que se llamó a [**IAMVideoAccelerator::BeginFrame,**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) proporcionando [**IAMVideoAccelerator::EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) no se ha llamado para ese índice de búfer de destino. Si DDI devuelve un estado de representación de DDERR WASSTCERTDRAWING para el búfer solicitado, se operará un bucle de suspensión en GetBuffer hasta que se \_ borra esta condición.  Para llamar a **GetBuffer,** el descodificador necesitará cierta información de una estructura de datos [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) que se obtiene mediante una llamada a [**IAMVideoAccelerator::GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo).
    -   [**IAMVideoAccelerator::Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) para indicar que se deben procesar los datos de un conjunto de búferes comprimidos como se indica en una matriz de estructuras de datos [**AMVABUFFERINFO.**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) En esta llamada se pasa al controlador un código de función dwFunction. También se pasa un puntero lpPrivateInputData a algunos datos para enviarlos de bajada y un puntero lpPrivateOutputData a un lugar donde el proceso de bajada puede colocar algunos datos para que el descodificador lea.
    -   [**IAMVideoAccelerator::ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) para indicar que el descodificador ha completado el uso de un búfer especificado por el momento y ya no necesita acceso bloqueado al búfer. (Si el descodificador desea seguir usando el búfer, simplemente no puede llamar a **IAMVideoAccelerator::ReleaseBuffer** por el momento, lo que evita la necesidad de llamar a [**IAMVideoAccelerator::GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) hasta que realmente pretende no usar el búfer más). El descodificador no debe escribir en el búfer después de llamar a [**Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) hasta que [**QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) indique que el búfer es seguro para escribir.
3.  Para completar el procesamiento de salida de un búfer de destino, el descodificador llama a [**IAMVideoAccelerator::EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe). Puede pasar algunos datos arbitrarios de bajada con esta llamada, y eso es básicamente todo lo que sucede como resultado de esta llamada. No envía un índice de búfer de destino en esta llamada, por lo que no puede indicar al acelerador con precisión qué búfer de destino se completa a menos que esta indicación esté contenida en los datos arbitrarios que se pasan.
4.  Para mostrar un marco, el descodificador llama a [**IAMVideoAccelerator::D isplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) con el índice del marco que se muestra y una estructura [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que contiene marcas de tiempo de inicio y detención y marcas **pertinentes, como dwTypeSpecificFlags** en la estructura [**PROPERTIES de AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) y **dwInterlaceFlags** en la [**estructura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) El descodificador debe comprobar que todas las operaciones de descompresión que afectan al contenido del marco se han completado antes de llamar **a DisplayFrame**.
5.  Por último, el descodificador debe, tras la finalización de todo el procesamiento, indicar la finalización de todos los fotogramas de salida iniciados restantes llamando a [**IAMVideoAccelerator::EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) y liberar todos sus búferes bloqueados mediante una llamada a [**IAMVideoAccelerator::ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) para cada búfer no publicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces y especificaciones del descodificador](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



