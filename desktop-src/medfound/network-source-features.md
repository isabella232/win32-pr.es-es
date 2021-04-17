---
description: Características de origen de red
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: Características de origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e937a97cf743740d9cebf84ad477c52cdee5083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554025"
---
# <a name="network-source-features"></a>Características de origen de red

El origen de red proporciona la implementación base para la transmisión por secuencias de archivos multimedia y expone la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . La implementación de origen de red específica depende del protocolo utilizado para abrir el origen como RTSP o HTTP. Los orígenes de red específicos del protocolo amplían la funcionalidad de red básica. Para obtener información sobre los esquemas y los protocolos admitidos, consulte [protocolos admitidos](supported-protocols.md).

El origen de red:

-   Implementa características como el almacenamiento en caché, la detección de proxy y la reconexión automática.
-   Convierte las llamadas independientes del Protocolo de la resolución de origen a llamadas específicas del protocolo.
-   Interactúa con la capa de sockets y el sistema operativo. Analiza la descripción de SDP y la usa como datos de configuración y Lee los datos de secuencia de la capa de sockets subyacentes. Al recibir, el origen de red es responsable de reordenar y solicitar las retransmisiones de paquetes.

## <a name="network-source-creation"></a>Creación de origen de red

La creación de un origen de medios para un origen de la red no es diferente de un origen de medios para un archivo local. La aplicación pasa la dirección URL del origen a los métodos de [resolución de origen](source-resolver.md) como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) y especifica la \_ marca MEDIASOURCE de la resolución MF \_ . Para obtener más información sobre el uso de esta marca, vea [usar el solucionador de origen](using-the-source-resolver.md).

Dependiendo del esquema proporcionado por la aplicación, la resolución de origen carga el objeto de controlador de esquema adecuado, que expone la interfaz [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . La aplicación también puede usar el controlador de esquema directamente para crear el origen de red mediante una llamada a [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

Para obtener más información, vea [controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Media Foundation no admite secuencias de bytes para orígenes de red. El objeto de flujo de bytes solo se admite en el escenario de contenido descargado. Todos los datos se transmiten lo más rápido posible para que se puedan guardar como un archivo en el equipo local. los servidores Web proporcionan datos descargados. No hay ninguna comunicación desde el cliente al servidor una vez iniciada la descarga. En este caso, se usa el protocolo de descarga HTTP.

Si la aplicación solicita que el solucionador de origen cree un objeto de flujo de bytes para los esquemas "http:", "MMS:" o "rtsp:", se produce un error en la llamada con el \_ error de esquema MF E \_ no compatible \_ .

> [!Note]  
> En Windows 7, el origen de red es compatible con los archivos de la estación de Windows Media (. NSC). Estos archivos se usan en la transmisión por secuencias de multidifusión del contenido multimedia a través de una red. Para crear el origen de red para un especificado. Archivo NSC, la aplicación debe utilizar la resolución de origen.

 

Si la aplicación usa el controlador de esquema, la llamada asincrónica omite el parámetro *dwFlags* y devuelve un puntero al origen de red al finalizar.

En la ilustración siguiente se muestra el flujo de datos para el streaming multimedia mediante el origen de red.

![diagrama de flujo que muestra las rutas de acceso de la aplicación al servidor de streaming, con un bucle entre el origen de red y la sesión multimedia](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>Configuración de origen de red

En este tema se describen las características admitidas por el origen de red y las opciones de configuración asociadas. Una aplicación puede configurar el origen de red al crear el objeto de origen de red. Estas opciones se almacenan en un objeto **IPropertyStore** , que la aplicación debe pasar en el parámetro *pProps* de los métodos de resolución de origen o [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

### <a name="auto-reconnect"></a>Reconexión automática

La característica de reconexión automática del origen de red permite a un cliente volver a conectarse al servidor multimedia automáticamente cuando se produce un error en la conexión TCP al servidor o cuando el cliente no puede recibir paquetes. Cuando se produce un error en la conexión, el origen de red intenta volver a conectarse al servidor multimedia con la misma configuración que se usó en la conexión anterior. El proceso de reconexión es asincrónico. El origen de red genera el evento [MEReconnectStart](mereconnectstart.md) cuando se inicia la reconexión y el evento [MEReconnectEnd](mereconnectend.md) cuando la reconexión se realiza correctamente o produce un error.

Si el número de intentos de reconexión supera el valor máximo especificado por la propiedad [**\_ AUTORECONNECTLIMIT de MFNETSOURCE**](mfnetsource-autoreconnectlimit-property.md) , se cancela la operación de reconexión. El número de intentos de reconexión se almacena en la propiedad [**MFNETSOURCE \_ AUTORECONNECTPROGRESS**](mfnetsource-autoreconnectprogress-property.md) .

La reconexión automática permite la reproducción fluida de contenido multimedia incluso cuando se produce un error en la conexión TCP al servidor multimedia. Para una experiencia de reproducción fluida, el cliente debe tener suficientes datos, al menos de 1 a 2 minutos, en su caché para continuar la reproducción hasta la reconexión. La cantidad máxima de datos que puede almacenar en búfer el origen de red se puede establecer en la propiedad [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) .

### <a name="fast-streaming"></a>Transmisión por secuencias rápida

El cliente de origen de red solicita al servidor que transmita algunos de los datos al principio del contenido con una tasa más rápida que la especificada en la velocidad de bits del contenido. Si el *Inicio rápido* está habilitado en el servidor, el servidor envía una secuencia de velocidad de bits acelerada para que el cliente pueda almacenar en búfer una cantidad suficiente de datos más rápido que en tiempo real. Esto mejora la experiencia del usuario al minimizar los retrasos de almacenamiento en búfer iniciales, lo que puede deberse a diversos factores, como la baja velocidad del equipo cliente o la red, y el ancho de banda disponible.

Para especificar la cantidad de datos de streaming rápido que el cliente puede solicitar, establezca la propiedad [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) . Si el origen de red usa UDP como protocolo de transporte, especifique la cantidad máxima de datos de streaming rápido mediante el establecimiento de la propiedad [**MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION**](mfnetsource-maxudpacceleratedstreamingduration-property.md) en su lugar.

El streaming rápido en el cliente también es posible a través de la característica de *caché rápida* : streaming a petición más rápido que el tiempo real y el almacenamiento en caché de los datos en la memoria caché local del cliente. Para usar este tipo de streaming rápido, la memoria caché rápida debe estar habilitada en el origen de red y el servidor debe ser compatible con ella. Cuando el cliente solicita contenido del servidor, el origen de red primero comprueba para ver si el contenido ya está en la memoria caché del cliente. Si el contenido está en la caché local del cliente y no ha expirado, se representa. Si el contenido no está en la memoria caché local o ya expiró, el contenido se transmite y se almacena en caché, y el origen de red lo reproduce desde la memoria caché local. En las solicitudes posteriores, para las listas de reproducción, solo se almacenan en caché y se reproducen las entradas que faltan. Si ya hay una entrada de lista de reproducción en la caché local del cliente, se reproduce desde allí y no se vuelve a almacenar en caché.

De forma predeterminada, la memoria caché rápida está habilitada en el cliente de origen de red. Sin embargo, los siguientes factores también determinan si se usa la característica:

-   El cliente debe tener un ancho de banda adicional disponible para descargar y almacenar en caché el contenido más rápido que la velocidad normal.
-   El cliente debe tener suficiente espacio en disco. Si el cliente tiene menos de 100 MB de espacio libre en disco después de almacenar en caché el contenido a petición solicitado, no se almacena en caché, sino que se transmite y se representa simultáneamente.

La característica de caché rápida se controla mediante la propiedad [**MFNETSOURCE \_ CACHEENABLED**](mfnetsource-cacheenabled-property.md) .

### <a name="buffer-management"></a>Administración de búfer

El origen de red proporciona una administración de búfer eficaz que supervisa el estado de búfer en el cliente. De forma predeterminada, el origen de red almacena en búfer 5 segundos de datos en el inicio. Este valor se puede configurar estableciendo la propiedad [**MFNETSOURCE \_ BUFFERINGTIME**](mfnetsource-bufferingtime-property.md) . Según el valor de esta propiedad, el origen de red calcula el tamaño de búfer suficiente para garantizar la reproducción fluida y sin interrupciones del contenido multimedia. Si esta propiedad se establece en 0, la administración del búfer está deshabilitada. Cuando la cantidad de contenido del búfer es baja, el origen de red comienza el almacenamiento en búfer y genera el evento [MEBufferingStarted](mebufferingstarted.md) para indicar que se ha iniciado el almacenamiento en búfer. Al recibir este evento, la canalización detiene la representación. Cuando se completa el almacenamiento en búfer, el origen de red genera el evento [MEBufferingStopped](mebufferingstopped.md) y el cliente puede comenzar a representarse de nuevo.

El cliente comienza a representar el contenido una vez que ha acumulado la cantidad de datos indicada por el tamaño del búfer de la primera muestra. Si este valor es menor que el tamaño de búfer calculado, la reproducción se inicia inmediatamente. Este comportamiento es muy similar a la característica de inicio rápido.

La propiedad [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) almacena la cantidad máxima de datos que se pueden almacenar en búfer.

### <a name="bandwidth-selection"></a>Selección de ancho de banda

Cuando un cliente se conecta al servidor multimedia, como parte de la configuración de la conexión, el origen *de red realiza una medición de pares de paquetes estáticos* para calcular el ancho de banda inicial del vínculo entre el cliente y el servidor. En función del resultado de esta medición, el cliente puede seleccionar secuencias de audio y vídeo que se ajusten al ancho de banda estimado. Esto garantiza una reproducción fluida del contenido multimedia de streaming.

Durante la fase de inicio rápido, se realiza la medición *dinámica de pares de paquetes* . En este proceso, el cliente recibe grandes cantidades de datos, que pueden ser varios paquetes o muestras.

El resultado de la medición dinámica de pares de paquetes es más preciso que la estimación de ancho de banda de vínculo devuelta por la medición de pares de paquetes estáticos porque el proceso de pares de paquetes estáticos envía un único paquete de tamaño fijo, lo que puede no producir resultados precisos para redes de ancho de banda alto.

La aplicación puede obtener el ancho de banda estimado mediante el uso de la propiedad [**MFNETSOURCE \_ PPBANDWIDTH**](mfnetsource-ppbandwidth-property.md) .

Las condiciones de red pueden cambiar dinámicamente, lo que provoca problemas de reproducción del origen de red. El origen de red puede cambiar la selección de flujo inicial del cliente en función de la velocidad de recepción y el estado del búfer. Por ejemplo, el cliente podría cambiar a una velocidad de bits inferior durante la congestión de la red y cambiar a una velocidad de bits más alta cuando el tráfico de red ha mejorado y el cliente ha acumulado una cantidad suficiente de contenido almacenado en búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



