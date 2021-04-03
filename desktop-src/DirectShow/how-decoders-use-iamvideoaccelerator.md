---
description: Cómo usan los descodificadores IAMVideoAccelerator
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Cómo usan los descodificadores IAMVideoAccelerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997639"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Cómo usan los descodificadores IAMVideoAccelerator

La interfaz [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) habilita las operaciones de aceleración de vídeo genéricas, incluida la aceleración de vídeo de DirectX (va). Para la aceleración que no es de DirectX, el controlador de vídeo y descodificador deben adherirse a un protocolo común.

En esta sección se describe el orden general de las operaciones que debe seguir cualquier descodificador al usar esta interfaz. Puede encontrar más información específica sobre los descodificadores basados en de DirectX VA en [asignación de aceleración de vídeo de DirectX a IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md).

> [!Note]  
> Esta interfaz está disponible en Windows 2000 y versiones posteriores.

 

La interfaz [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) se expone en el PIN de entrada del [mezclador de superposición](overlay-mixer-filter.md) o el procesador de mezcla de vídeo (VMR). La interfaz [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) se expone en el PIN de salida del descodificador. La secuencia de eventos para la conexión de los PIN del filtro es la siguiente:

1.  El administrador de gráficos de filtro llama a [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) en el PIN de salida del filtro del descodificador. Un [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) es un parámetro opcional.
    -   [**AM \_ El \_ tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type) es una estructura de datos que describe un tipo de medio. Contiene un GUID de majortype (que, en nuestro caso, debe ser un vídeo de MEDIATYPE \_ ), un GUID de subtipo (que en nuestro caso debe ser un GUID de acelerador de vídeo) y otras muchas cosas. Una de estas cosas es un GUID de tipo de formato que contiene información sobre los medios, incluido en nuestro caso, el ancho y el alto de una imagen de vídeo sin comprimir, probablemente en una estructura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
    -   La estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , si está presente, indica al descodificador que opere con el tipo de medio especificado, que puede ser "totalmente especificado" o "especificado parcialmente". Si se especifica "Full", el descodificador simplemente intentaría trabajar con ese tipo de medio. Si "se ha especificado parcialmente", intentará encontrar un modo de operación compatible "totalmente especificado" que pueda usar para conectarse de forma coherente con el tipo de medio "especificado parcialmente".
    -   La manera habitual de intentar encontrar un tipo de medio "totalmente especificado" para usar en una conexión es simplemente ejecutar una lista de todos los tipos de medios "totalmente especificados" que admite el PIN de salida, que es compatible con el tipo de medio "especificado parcialmente" e intenta conectarse a cada uno de ellos hasta que se realiza correctamente. Normalmente, el proceso sería similar si no \_ \_ se incluye ningún tipo de medio am en la llamada a [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , pero con el PIN de salida que necesita comprobar todos sus tipos de medios.
2.  Si el descodificador desea comprobar si un [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) específico (incluido un GUID de acelerador de vídeo) es compatible con el PIN de entrada de nivel inferior, puede llamar a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (con el GUID de acelerador de vídeo como el subtipo del **\_ \_ tipo de medio am**) o simplemente intentar conectarse a ese pin tal y como se describe en el elemento 5.
3.  Si el descodificador no sabe qué GUID de acelerador de vídeo admite el PIN de entrada de nivel inferior y no desea proponer solo un GUID de acelerador de vídeo candidato determinado llamando a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)del PIN de entrada de nivel inferior, el descodificador puede llamar a [**IAMVideoAccelerator:: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) para obtener una lista de los GUID del acelerador de vídeo que admite el PIN.
4.  Para algunos GUID de acelerador de vídeo determinados, el descodificador puede llamar a [**IAMVideoAccelerator:: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) del PIN de entrada de nivel inferior para obtener una lista de los formatos de píxeles de **DDPIXELFORMAT** que se pueden usar para representar un GUID de acelerador de vídeo específico. La lista devuelta debe considerarse en orden de preferencia decreciente (es decir, con el formato más preferido indicado en primer lugar).
5.  El descodificador llama a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)del PIN de entrada de nivel inferior, pasándole un [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) con el GUID de acelerador de vídeo adecuado como el subtipo del tipo de medio. Esto configura la conexión para la operación, incluida la creación de las superficies de salida sin comprimir (que se asignan con el ancho y el alto que se encuentran en el **\_ \_ tipo de medio am** y el número de superficies que se asignan en una llamada que se describe a continuación, y cualquier otra información que el acelerador de vídeo tenga disponible y desee usar para ese propósito, como el propio GUID de Si el PIN de entrada de nivel inferior rechaza el GUID de acelerador de vídeo o algún otro aspecto de la conexión, puede producirse un error en **IPin:: ReceiveConnection** . Si **IPin:: ReceiveConnection** produce un error, esto se indica en un **HRESULT** devuelto y el descodificador puede intentar realizar la llamada de nuevo, por ejemplo, con un nuevo GUID de acelerador de vídeo en la estructura de **\_ \_ tipo de medio am** .
    -   [!Note]  
        > Esta es otra manera (y la forma más definitiva) para que el descodificador determine qué es compatible con el PIN de entrada de nivel inferior, simplemente llamando a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e intentando conectarse y, a continuación, comprobando si el intento de conexión se realizó correctamente.

         

    -   Durante el [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection), el representador llama a [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)del descodificador, pasándole el GUID del acelerador de vídeo y una estructura [**AMVAUncompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) para averiguar el número de superficies sin comprimir que se van a asignar. El descodificador rellena y devuelve la estructura, que contiene el número mínimo y máximo de superficies que se van a asignar del tipo determinado, y una estructura **DDPIXELFORMAT** que describe el formato de píxel de las superficies que se van a asignar.
    -   [!Note]  
        > En realidad, no se pasa nada al descodificador en la llamada a [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) que no sea el GUID del acelerador de vídeo.

         

6.  El representador llama al [**IAMVideoAcceleratorNotify:: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)del descodificador, pasando al descodificador el número real de superficies sin comprimir que se asignaron.
7.  El representador llama a [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) del descodificador para obtener los datos necesarios para inicializar el acelerador de vídeo.
8.  El descodificador llama a [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo), pasándole un GUID de acelerador de vídeo, una estructura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) y el número de tipos de búfer comprimidos, para obtener un conjunto de estructuras de datos [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) , uno correspondiente a cada tipo de búfer de datos comprimidos utilizado por el GUID del acelerador de vídeo.
    -   La estructura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) contiene el ancho y el alto de los datos sin comprimir descodificados (en píxeles) y el DDPIXELFORMAT de la imagen sin comprimir.
    -   Las estructuras de datos [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) devueltas contienen:
        -   El número de búferes comprimidos necesarios para el tipo específico.
        -   Ancho y alto de la superficie que se va a crear (campos que pueden tener o no un significado real).
            > [!Note]  
            > La operación de asignación de superficie de DirectDraw para los búferes comprimidos no proporciona actualmente el ancho o el alto de estas superficies para ser mayor o igual que 2 ^ 15, aunque es posible que la llamada de asignación de superficie no falle de forma abierta si se infringe este límite. Por lo tanto, el controlador podría estructurar sus solicitudes de memoria de búfer comprimida para evitar los tamaños extremos. Por ejemplo, en lugar de solicitar un búfer con width = "1" y height = "65536", el controlador debe solicitar un búfer de width = "1024" y height = "64".

             

        -   Número total de bytes que va a usar la superficie.
        -   Estructura de tipo **DDSCAPS2** que define un objeto DirectDrawSurface, que describe las funciones para crear superficies para almacenar datos comprimidos.
        -   Un DDPIXELFORMAT, que describe el formato de píxel que se usa para crear superficies para almacenar datos comprimidos (un campo que puede tener o no un significado real).

> [!Note]  
> Las llamadas del representador a algunos de los métodos de interfaz [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) del descodificador pueden (y normalmente) aparecer dentro de la llamada del descodificador a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)del representador. En concreto, esto se aplica a lo siguiente:
>
> -   [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**IAMVideoAcceleratorNotify:: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)y
> -   [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Para admitir los cambios de formato dinámico, el descodificador también puede llamar a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) y otros métodos por encima mientras los filtros están conectados y en ejecución. Esta funcionalidad se proporciona para admitir los cambios de formato dinámico (aunque no se encuentran en H. 263, anexo P, es decir, ya que todos los conjuntos de datos se inician de nuevo desde cero y, por tanto, se pierde cualquier información de imagen de referencia).

 

A continuación se describe el uso de [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) durante la operación después de la inicialización:

1.  Para cada superficie sin comprimir, el descodificador llama a [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) para comenzar el procesamiento y crear la imagen de salida. Cuando lo hace, el descodificador envía una estructura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) .
    -   La estructura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) contiene un índice para un búfer de destino, un puntero a algunos datos que se van a enviar de nivel inferior y un puntero a un lugar donde el acelerador puede colocar algunos datos para que el descodificador pueda leerlos.
    -   Nota 1: el Acelerador realmente no recibe el índice de búfer de destino, ya que lo traduce el representador antes de pasar al nivel inferior.
    -   Nota 2: [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) se puede llamar más de una vez entre las llamadas a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe).
    -   Nota 3: no hay ninguna suposición dentro de la operación de interfaz que sea necesario llamar a [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) y [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) para el procesamiento de cada imagen individual en el fragmentada.

        Lo que [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) hace, en lo que se refiere a la interfaz, es crear una asociación dentro del representador entre un índice y una superficie sin comprimir. También proporciona un medio para llamar a una función específica en un controlador de dispositivo (compatible con un medio de pasar datos arbitrarios entre el descodificador y el controlador de dispositivo).

        (Sin embargo, en la operación de DirectX VA hay un requisito que se describe a continuación que se debe llamar a [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) y [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) para el procesamiento de cada imagen individual en el fragmentada).

2.  Para enviar datos sin comprimir al acelerador, el descodificador llama a:
    -   [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) para determinar si un búfer es seguro para leer o escribir en él.
    -   [**IAMVideoAccelerator:: getBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) para bloquear y obtener acceso a un búfer especificado (si no lo ha llamado previamente para obtener ese acceso). **GetBuffer** también se puede usar para obtener una copia del contenido de la última imagen de salida sin comprimir para la que se llamó a [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , ya que no se ha llamado a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) para ese índice de búfer de destino. Si DDI devuelve un estado de representación de DDERR \_ WASSTILLDRAWING para el búfer solicitado, se operará un bucle de suspensión dentro de **getBuffer** hasta que se desactive esta condición. Para llamar a **getBuffer**, el descodificador necesitará cierta información de una estructura de datos [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) que se obtiene llamando a [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo).
    -   [**IAMVideoAccelerator:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) para indicar que se deben procesar los datos de un conjunto de búferes comprimidos, tal y como se indica en una matriz de estructuras de datos [**AMVABUFFERINFO**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) . Un dwFunction de código de función se pasa al controlador en esta llamada. También se pasa un puntero lpPrivateInputData a algunos datos para enviar el nivel inferior, y se pasa un puntero lpPrivateOutputData a un lugar donde el proceso de nivel inferior puede poner algunos datos para que el descodificador pueda leerlos.
    -   [**IAMVideoAccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) para indicar que el descodificador ha completado el uso de un búfer especificado durante el tiempo y ya no necesita acceso bloqueado al búfer. (Si el descodificador desea seguir usando el búfer, simplemente no puede llamar a **IAMVideoAccelerator:: ReleaseBuffer** por el momento, lo que evita la necesidad de llamar a [**IAMVideoAccelerator:: getBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) hasta que realmente realmente intenta no usar el búfer). El descodificador no debe escribir en el búfer después de llamar a [**Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) hasta que [**QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) indique que el búfer es seguro para escritura.
3.  Para completar el procesamiento de salida para un búfer de destino, el descodificador llama a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe). Puede pasar algunos datos arbitrarios de nivel inferior con esta llamada y, esencialmente, todo esto sucede como resultado de esta llamada. No envía un índice de búfer de destino en esta llamada, por lo que no puede indicar al acelerador exactamente qué búfer de destino se ha completado a menos que esta indicación esté contenida en los datos arbitrarios que se pasan.
4.  Para mostrar un fotograma, el descodificador llama a [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) con el índice del marco que se va a mostrar y una estructura [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que contiene las marcas de tiempo de inicio y detención y las marcas pertinentes, como **dwTypeSpecificFlags** en la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) , y **dwInterlaceFlags** en la estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . El descodificador debe comprobar que todas las operaciones de descompresión que afectan al contenido del marco se han completado antes de llamar a **DisplayFrame**.
5.  Por último, el descodificador debe, tras la finalización de todo el procesamiento, indicar la finalización de todos los fotogramas de salida que se han iniciado, llamando a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) y libera todos sus búferes bloqueados llamando a [**IAMVideoAccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) para cada búfer sin liberar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces y especificaciones del descodificador](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



