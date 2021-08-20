---
description: Características de origen de red
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: Características de origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a06b945f82093d5ff235eef306768e68b9f9771a2816df9a4580adab2d8dde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871898"
---
# <a name="network-source-features"></a>Características de origen de red

El origen de red proporciona la implementación base para los archivos multimedia de streaming y expone la [**interfaz DEFUTMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) La implementación de origen de red específica depende del protocolo utilizado para abrir el origen, como RTSP o HTTP. Los orígenes de red específicos del protocolo amplían la funcionalidad de red básica. Para obtener información sobre los esquemas y protocolos admitidos, vea [Protocolos admitidos.](supported-protocols.md)

Origen de red:

-   Implementa características como el almacenamiento en caché, la detección de proxy y la reconexión automática.
-   Convierte las llamadas independientes del protocolo de la resolución de origen en llamadas específicas del protocolo.
-   Interactúa con la capa de socket y el sistema operativo. Analiza la descripción de SDP, la usa como datos de configuración y lee los datos de flujo de la capa de sockets subyacente. Cuando se recibe, el origen de red es responsable de reordenar y solicitar retransmisiones de paquetes.

## <a name="network-source-creation"></a>Creación de origen de red

La creación de un origen multimedia para un origen de la red no es diferente de un origen multimedia para un archivo local. La aplicación pasa la dirección URL del origen a métodos de [resolución](source-resolver.md) de origen, como [**MFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o [**MFSourceResolver::BeginCreateObjectFromURL,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) y especifica la marca MF \_ RESOLUTION \_ MEDIASOURCE. Para obtener más información sobre el uso de esta marca, vea [Usar el solucionador de origen](using-the-source-resolver.md).

Según el esquema proporcionado por la aplicación, el solucionador de origen carga el objeto de controlador de esquema adecuado, que expone la interfaz [**ODBCSchemeHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) La aplicación también puede usar el controlador de esquema directamente para crear el origen de red llamando a [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

Para obtener más información, vea [Scheme Handlers and Byte-Stream Handlers](scheme-handlers-and-byte-stream-handlers.md).

Media Foundation no admite secuencias de bytes para orígenes de red. El objeto de secuencia de bytes solo se admite en el escenario de contenido descargado. Todos los datos se transmiten lo más rápido posible para que se puedan guardar como un archivo en el equipo local. los servidores web proporcionan datos descargados. No hay ninguna comunicación del cliente con el servidor después de que comience la descarga. En este caso, se usa el protocolo de descarga HTTP.

Si la aplicación solicita al solucionador de origen que cree un objeto de secuencia de bytes para los esquemas "http:", "mms:" o "rtsp:", se produce un error en la llamada con el error MF \_ E \_ UNSUPPORTED \_ SCHEME.

> [!Note]  
> En Windows 7, el origen de red admite archivos Windows Media Station (. NSC). Estos archivos se usan en el streaming de multidifusión de contenido multimedia a través de una red. Para crear el origen de red para un especificado. Archivo NSC, la aplicación debe usar la resolución de origen.

 

Si la aplicación usa el controlador de esquema, la llamada asincrónica omite el parámetro *dwFlags* y devuelve un puntero al origen de red al finalizar.

En la ilustración siguiente se muestra el flujo de datos para el streaming multimedia mediante el origen de red.

![diagrama de flujo que muestra las rutas de acceso de la aplicación al servidor de streaming, con un bucle entre el origen de red y la sesión multimedia](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>Configuración de origen de red

En este tema se describen las características admitidas por el origen de red y las opciones de configuración asociadas. Una aplicación puede configurar el origen de red al crear el objeto de origen de red. Estas opciones se almacenan en un objeto **IPropertyStore,** que la aplicación debe pasar en el *parámetro pProps* de los métodos de resolución de origen o [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

### <a name="auto-reconnect"></a>Reconexión automática

La característica de reconexión automática del origen de red permite a un cliente volver a conectarse al servidor multimedia automáticamente cuando se produce un error en la conexión TCP con el servidor o cuando el cliente no recibe paquetes. Cuando se produce un error en la conexión, el origen de red intenta volver a conectarse al servidor multimedia con la misma configuración que se usó en la conexión anterior. El proceso de reconexión es asincrónico. El origen de red genera el [evento MEReconnectStart](mereconnectstart.md) cuando comienza la reconexión y el evento [MEReconnectEnd](mereconnectend.md) cuando la reconexión se realiza correctamente o produce un error.

Si el número de intentos de reconexión supera el valor máximo especificado por la propiedad [**MFNETSOURCE \_ AUTORECONNECTLIMIT,**](mfnetsource-autoreconnectlimit-property.md) se cancela la operación de reconexión. El número de intentos de reconexión se almacena en la [**propiedad MFNETSOURCE \_ AUTORECONNECTPROGRESS.**](mfnetsource-autoreconnectprogress-property.md)

La reconexión automática permite una reproducción fluida del contenido multimedia incluso cuando se produce un error en la conexión TCP con el servidor multimedia. Para una experiencia de reproducción fluida, el cliente debe tener suficientes datos, al menos de 1 a 2 minutos, en su memoria caché para continuar la reproducción hasta que se vuelva a conectar. La cantidad máxima de datos que el origen de red puede almacenar en búfer se puede establecer en la [**propiedad MFNETSOURCE \_ MAXBUFFERTIMEMS.**](mfnetsource-maxbuffertimems-property.md)

### <a name="fast-streaming"></a>Streaming rápido

El cliente de origen de red solicita al servidor que transmita algunos de los datos al principio del contenido a una velocidad más rápida que la especificada por la velocidad de bits del contenido. Si *el inicio rápido* está habilitado en el servidor, el servidor envía un flujo de velocidad de bits acelerada para que el cliente pueda almacenar en búfer una cantidad suficiente de datos más rápido que en tiempo real. Esto mejora la experiencia del usuario al minimizar los retrasos iniciales del almacenamiento en búfer, que pueden deberse a diversos factores, como la baja velocidad del equipo cliente o la red, y el ancho de banda disponible.

Para especificar la cantidad de datos de streaming rápido que el cliente puede solicitar, establezca la propiedad [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION.**](mfnetsource-acceleratedstreamingduration-property.md) Si el origen de red usa UDP como protocolo de transporte, especifique la cantidad máxima de datos de streaming rápido estableciendo en su lugar la propiedad [**MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION.**](mfnetsource-maxudpacceleratedstreamingduration-property.md)

El streaming rápido en el cliente también es posible a través de la característica *Caché* rápida: streaming de contenido a petición más rápido que en tiempo real y almacenamiento en caché de datos en la memoria caché local del cliente. Para usar este tipo de streaming rápido, la caché rápida debe estar habilitada en el origen de red y el servidor debe admitirlo. Cuando el cliente solicita contenido del servidor, el origen de red comprueba primero si el contenido ya está en la memoria caché del cliente. Si el contenido está en la caché local del cliente y no ha expirado, se representa. Si el contenido no está en la caché local o ya ha expirado, el contenido se transmite y se almacena en caché, y el origen de red lo reproduce desde la caché local. En las solicitudes posteriores, para las listas de reproducción, solo se almacenan en caché las entradas que faltan y, a continuación, se reproducen. Si una entrada de lista de reproducción ya está en la caché local del cliente, se reproduce desde allí y no se vuelve a almacenar en caché.

De forma predeterminada, Fast Cache está habilitado en el cliente de origen de red. Sin embargo, los siguientes factores también determinan si se usa la característica:

-   El cliente debe tener ancho de banda adicional disponible para descargar y almacenar en caché el contenido más rápido que la velocidad normal.
-   El cliente debe tener suficiente espacio en disco. Si el cliente tiene menos de 100 MB de espacio libre en disco después de almacenar en caché el contenido a petición solicitado, no se almacena en caché, sino que se transmite y se representa simultáneamente.

La característica Caché rápida se controla mediante la [**propiedad MFNETSOURCE \_ CACHEENABLED.**](mfnetsource-cacheenabled-property.md)

### <a name="buffer-management"></a>Administración de búfer

El origen de red proporciona una administración eficaz del búfer que supervisa el estado del búfer en el cliente. De forma predeterminada, el origen de red almacena en búfer 5 segundos de datos en el inicio. Este valor se puede configurar estableciendo la [**propiedad MFNETSOURCE \_ BUFFERINGTIME.**](mfnetsource-bufferingtime-property.md) Según este valor de propiedad, el origen de red calcula el tamaño de búfer suficiente para garantizar una reproducción fluida e ininterrumpida del contenido multimedia. Si esta propiedad se establece en 0, la administración de búferes está deshabilitada. Cuando la cantidad de contenido del búfer es baja, el origen de red inicia el almacenamiento en búfer y genera el evento [MEBufferingStarted](mebufferingstarted.md) para indicar que ha comenzado el almacenamiento en búfer. Al recibir este evento, la canalización deja de representarse. Una vez completado el almacenamiento en búfer, el origen de red genera el evento [MEBufferingStopped](mebufferingstopped.md) y el cliente puede empezar a representarse de nuevo.

El cliente comienza a representar el contenido después de haber acumulado la cantidad de datos indicados por el tamaño de búfer de la primera muestra. Si este valor es inferior al tamaño de búfer calculado, la reproducción se inicia inmediatamente. Este comportamiento es muy similar a la característica Inicio rápido.

La [**propiedad MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) almacena la cantidad máxima de datos que se pueden almacenar en búfer.

### <a name="bandwidth-selection"></a>Selección de ancho de banda

Cuando un cliente se conecta al servidor multimedia, como parte de la configuración de la conexión, el origen de red realiza una medición estática del par de *paquetes* para calcular el ancho de banda de vínculo inicial entre el cliente y el servidor. En función del resultado de esta medida, el cliente puede seleccionar secuencias de audio y vídeo que se ajusten al ancho de banda estimado. Esto garantiza una reproducción fluida del contenido multimedia de streaming.

Durante la fase de inicio rápido, *se realiza la medición dinámica de pares de* paquetes. En este proceso, el cliente recibe grandes cantidades de datos, que pueden ser varios paquetes o ejemplos.

El resultado de la medición dinámica del par de paquetes es más preciso que la estimación de ancho de banda de vínculo devuelta por la medida estática de par de paquetes porque el proceso estático de par de paquetes envía un único paquete de tamaño fijo, lo que puede no producir resultados precisos para redes de ancho de banda alto.

La aplicación puede obtener el ancho de banda estimado mediante la propiedad [**MFNETSOURCE \_ PPBANDWIDTH.**](mfnetsource-ppbandwidth-property.md)

Las condiciones de red pueden cambiar dinámicamente, lo que provoca problemas en la reproducción del origen de red. El origen de red puede cambiar la selección de secuencia inicial del cliente en función de la velocidad de recepción y el estado del búfer. Por ejemplo, el cliente podría cambiar a una velocidad de bits inferior durante la congestión de la red y volver a una velocidad de bits más alta cuando el tráfico de red ha mejorado y el cliente ha acumulado una cantidad suficiente de contenido almacenado en búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



