---
description: Media Foundation proporciona el origen multimedia de ASF que una aplicación puede usar para representar un archivo ASF en la capa de canalización de la arquitectura.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Origen multimedia de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75dc682d48339ce4ff707e7859a6962b9f5cfd92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360716"
---
# <a name="asf-media-source"></a>Origen multimedia de ASF

Media Foundation proporciona el origen multimedia de ASF que una aplicación puede usar para representar un archivo ASF en la capa de canalización de la arquitectura.

Para reproducir un archivo ASF, una aplicación puede usar el origen multimedia de ASF para alimentar los datos en una canalización de reproducción. En un escenario de codificación, la aplicación puede usar el origen multimedia de ASF como origen para convertir a otro formato o para convertir un archivo de velocidad de bits superior en un archivo de velocidad de bits inferior sin cambiar los formatos. El origen de medios de ASF debe usarse en la capa de canalización, es decir, una aplicación debe usar la sesión multimedia para controlar la operación. Este nivel de acceso permite a las aplicaciones obtener eventos mientras la sesión multimedia está en curso. Para obtener acceso de nivel inferior al contenido de ASF, una aplicación debe usar los componentes de ASF de la capa WMContainer.

El origen multimedia de ASF implementa la interfaz [**IMFMediaSource,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que es la interfaz genérica para los orígenes multimedia de Media Foundation. Al igual que cualquier otro origen de medios, el origen multimedia de ASF proporciona un descriptor de presentación que describe principalmente el objeto de encabezado de ASF. Además, el origen multimedia de ASF proporciona descriptores de flujo que representan cada secuencia en el contenido multimedia. Para obtener más información, vea [ASF File Structure](asf-file-structure.md).

-   [Creación del origen de medios de ASF](#creating-the-asf-media-source)
-   [Configuración Configuración para el origen de medios de ASF](#configuration-settings-for-the-asf-media-source)
-   [Modelo de objetos de origen multimedia de ASF](#asf-media-source-object-model)
-   [Servicios de origen multimedia de ASF](#asf-media-source-services)
    -   [Traducción de código de tiempo](#timecode-translation)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-asf-media-source"></a>Creación del origen de medios de ASF

Para crear el origen de medios de ASF, la aplicación debe usar el [solucionador de origen](source-resolver.md). Para crear el origen de medios de ASF, la aplicación debe proporcionar el origen para el que el solucionador de origen crea el origen de medios de ASF. La información de origen debe proporcionarse especificando la dirección URL del archivo de origen o la secuencia de bytes que contiene el medio. Si la aplicación elige crear el origen de medios de ASF especificando la dirección URL, debe llamar a LA DIRECCIÓN URL DE LA OPERACIÓN sincrónica [**DEFUSSOURCEResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para una operación sincrónica o **ASESOURCEResolver::Begin... EndCreateObjectFromURL para** la operación asincrónica. El proceso para crear el origen multimedia a partir de una secuencia de bytes es similar. La aplicación debe llamar [**a IMFSourceResolver::CreateObjectFromByteStream para**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) una operación sincrónica o **a IMFSourceResolver::Begin... EndCreateObjectFromBytestream para** la operación asincrónica. Estas llamadas deben especificar MF \_ RESOLUTION \_ MEDIASOURCE en *el parámetro dwFlags.* Para obtener más información sobre el uso de esta marca, vea Usar el solucionador de origen.

Si la aplicación especifica una dirección URL, para un archivo local, la cadena de dirección URL puede contener la ruta de acceso del archivo multimedia o puede tener el prefijo "file: "scheme. La extensión de nombre de archivo debe ser ".asf", ".wm", L".wma" o ".wmv". Para un archivo ASF en la red, la resolución de origen crea el origen [de red](network-source-features.md), que usa el origen de medios de ASF.

Durante el proceso de creación de objetos, la resolución de origen busca la lista de controladores de esquema y los controladores de flujo de bytes en el registro del sistema y carga el controlador de coincidencia más cercano que puede analizar el contenido multimedia y también crear el objeto de origen multimedia debajo. Independientemente del método usado para crear el origen multimedia (url y secuencia de bytes), el solucionador de origen crea una secuencia de bytes y lee el contenido de los medios de origen en la secuencia de bytes. Para obtener más información, vea [Scheme Handlers and Byte-Stream Handlers](scheme-handlers-and-byte-stream-handlers.md).

Para obtener un ejemplo de código sobre cómo crear un origen multimedia, vea [Using the Source Resolver](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Configuración Configuración para el origen de medios de ASF

La resolución de origen consulta las funciones de la secuencia de bytes subyacente y determina que las operaciones se permiten en el origen multimedia recién creado. Una de estas funcionalidades es la búsqueda. Si se permite una operación de búsqueda, la aplicación puede especificar el modo de búsqueda que usa el origen multimedia al buscar en un punto determinado de la presentación.

Una aplicación puede establecer el modo de búsqueda, para que el origen multimedia lo use, durante la creación del objeto. Una vez creado el origen de medios de ASF con el modo de búsqueda especificado, no se puede modificar en el origen de medios ni cambiar dinámicamente durante una presentación. Las preferencias de búsqueda se especifican como propiedades en la llamada de la aplicación a los métodos de resolución de origen pertinentes que se usan para crear el origen multimedia. Este conjunto de propiedades se establece en un almacén de propiedades y se pasa al *parámetro pProps.* Si no se pasan estas propiedades, el origen multimedia funciona con la configuración predeterminada. Para obtener más información sobre cómo establecer estas propiedades, vea [Configuring a Media Source](configuring-a-media-source.md).

Si se permite la búsqueda, el origen multimedia de ASF admite los siguientes modos de búsqueda:

-   Búsqueda exacta: en este modo, el origen multimedia de ASF se basa en el objeto de índice de ASF del archivo ASF. Si el archivo no tiene el objeto de índice, se deshabilita la búsqueda exacta y uno de los otros modos se usa en función de las propiedades especificadas por la aplicación que se establecen en el origen multimedia.
-   Búsqueda aproximada: la aplicación solicita este modo pasando [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) en el almacén de propiedades a los métodos de resolución de origen pertinentes. Sin embargo, la búsqueda aproximada solo se usa si la secuencia de bytes no admite búsquedas basadas en tiempo. En este modo, el origen multimedia determina una hora de inicio relativamente más cercana a la hora de búsqueda. Si el archivo ASF contiene un objeto de índice de ASF, se usa para calcular la hora de inicio. La búsqueda aproximada es menos precisa, pero más rápida que la búsqueda exacta, ya que el tiempo que se toma para representar la primera muestra a la hora de inicio predeterminada es más rápido.
-   Búsqueda iterativa: para establecer este modo, la aplicación debe establecer la propiedad [ \_ ASFMediaSource \_ IterativeSeekIfNoIndex de MFPKEY.](mfpkey-asfmediasource-iterativeseekifnoindex.md) La búsqueda iterativa es un algoritmo para buscar una posición en un archivo ASF que no contiene ningún objeto de índice de ASF. En este modo, el origen multimedia determina una estimación aproximada del punto de búsqueda mediante la lectura del desplazamiento de la secuencia de bytes. Usa una serie de aproximaciones, basadas en la velocidad de bits media, para acercarse progresivamente al tiempo de búsqueda de destino. (El algoritmo es similar a una búsqueda binaria). La búsqueda iterativa puede tardar más que la búsqueda mediante el objeto index, por lo que está deshabilitada de forma predeterminada. Si establece esta propiedad, use las siguientes propiedades para establecer los parámetros de búsqueda: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance In \_ \_ MilliSecond](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Estas propiedades establecen el número máximo de iteraciones y la tolerancia, respectivamente. El algoritmo se detiene cuando alcanza el número máximo de iteraciones o cuando encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada.

En pocas palabras, la aplicación tiene la opción de elegir la búsqueda aproximada o iterativa cuando el archivo ASF no contiene un objeto de índice de ASF.

## <a name="asf-media-source-object-model"></a>Modelo de objetos de origen multimedia de ASF

El origen multimedia de ASF implementa la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) y expone las interfaces siguientes. Una aplicación puede obtener una referencia a estas interfaces llamando a **IMFMediaSource::QueryInterface** en el origen multimedia de ASF.



| Interfaz                                                | Descripción                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Obligatorio para todos los orígenes de medios.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obligatorio para todos los orígenes de medios. Permite a las aplicaciones obtener eventos del origen de medios a través de la sesión multimedia.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Consulta el origen de medios para la interfaz de servicio especificada.                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Establece y obtiene propiedades en el origen de medios. Cada propiedad contiene un nombre descriptivo y un valor.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Describe los metadatos del archivo ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Recupera una colección de metadatos, ya sea para una presentación completa o para una secuencia de la presentación.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Consulta el intervalo de velocidades de reproducción que se admiten, incluida la reproducción inversa.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Obtiene o establece la velocidad de reproducción.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Obtiene el ITA para cada una de las secuencias de ASF contenidas en el origen.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Permite que un origen de medios reciba un puntero a la interfaz [**DEHOMPHost,**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) que se usa para crear objetos en el proceso PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Convierte los códigos de tiempo de la Sociedad de imágenes de movimiento e ingenieros de televisión (SMPTE) y las unidades de tiempo de 100 nanosegundos.                              |



 

## <a name="asf-media-source-services"></a>Servicios de origen multimedia de ASF

El origen multimedia de ASF proporciona varios servicios con ámbito para el archivo ASF. Para obtener un puntero a un servicio determinado, la aplicación debe usar uno de los siguientes identificadores de servicio en su llamada a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Para obtener información, vea [Interfaces de servicio](service-interfaces.md).



| Identificador de servicio               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ RATE \_ CONTROL \_ SERVICE       | Con este identificador, una aplicación puede obtener un puntero a las interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) [**o IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Mediante el uso del objeto de compatibilidad de velocidad implementado por el origen de medios, la aplicación puede comprobar si una velocidad determinada es compatible con el archivo multimedia de ASF subyacente también obtiene la velocidad más rápida y más lenta. Mediante el uso del objeto de control de velocidad, la aplicación puede obtener y establecer la velocidad de reproducción. Si la aplicación especifica una velocidad determinada para la reproducción, el origen multimedia de ASF comprueba primero si la velocidad solicitada está dentro de los límites de velocidad (determinados por las velocidades más rápidas y más lentas) y, a continuación, establece la velocidad. Esto no comprueba las condiciones variables, ya que la velocidad de bits puede cambiar en cualquier momento en función del ancho de banda de red. Para obtener más información, consulte [Control de velocidad.](rate-control.md) |
| SERVICIO MF \_ METADATA \_ \_ PROVIDER  | Con este identificador, la aplicación puede obtener un puntero a la interfaz [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) del origen de medios de ASF. Esta interfaz proporciona acceso a información sobre el archivo ASF específicamente los objetos de encabezado de ASF y las secuencias contenidas en el contenido multimedia. La información de encabezado se expone a través de atributos de descriptor de presentación y la información de secuencia se proporciona a través de atributos de descriptor de flujo. Para obtener más información sobre estos atributos, [vea atributos Media Foundation para objetos de encabezado de ASF.](media-foundation-attributes-for-asf-header-objects.md) Además de la información que se expone a través de atributos, también existen metadatos descriptivos, que se establecen como propiedades.                                                                                                 |
| SERVICIO DE \_ CONTROLADOR \_ DE PROPIEDADES \_ MF   | Con este identificador, la aplicación puede obtener un puntero a la [**interfaz IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) del origen de medios de ASF. El almacén de propiedades contiene todos los metadatos relacionados con el archivo ASF. Este identificador es nuevo en Windows 7 y reemplaza MF \_ METADATA PROVIDER SERVICE para obtener las propiedades de \_ \_ metadatos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SERVICIO DE \_ ESTADÍSTICAS MFNETSOURCE \_ | Para obtener más información, vea Retrieving Network Statistics in [Client Logging](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SERVICIO \_ MF TIMECODE \_            | Con este identificador, la aplicación puede obtener un puntero a la interfaz [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) del origen multimedia. Esta implementación se puede usar para realizar traducciones de código de tiempo, como convertir código de tiempo SMPTE en unidades de 100 nano segundos y atrás.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Traducción de códigos de tiempo

El origen multimedia de ASF proporciona un servicio de traducción de código de tiempo que permite a la aplicación convertir el código de hora de SMPTE al tiempo de presentación más cercano (en una unidad de 100 nanosegundos). Por el contrario, la aplicación también puede obtener el código de hora para un tiempo de presentación solicitado. El servicio está disponible a través de [**la interfaz IMFTimecodeTranslate,**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) que implementa el origen de medios de ASF. Las llamadas de método en este puntero de interfaz son asincrónicas que se pueden ejecutar desde el subproceso de aplicación principal sin bloquear la interfaz de usuario de la aplicación.

En los pasos siguientes se resume el procedimiento para la traducción de código de tiempo:

1.  Obtenga el puntero a la interfaz [**MFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) del origen multimedia de ASF llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y especificando el identificador **DEL SERVICIO MF \_ TIMECODE. \_**
2.  Llame [**a IMFTimecodeTranslate::BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) o [**a IMFTimecodeTranslate::BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) y especifique la hora que se va a traducir. Para **BeginConvertTimecodeToHNS,** el código de hora debe especificarse como una variable [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) con el tipo de **datos VT \_ I8.** El **método BeginConvertHNSToTimecode** requiere el tiempo en unidades de 100 nanosegundos como el [**tipo MFTIME.**](mftime.md)
3.  Complete la operación asincrónica mediante una llamada [**a IMFTimecodeTranslate::EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) o **a IMFTimecodeTranslate::EndConvertTimecodeToHNS** correctamente.

Durante la creación del origen de medios, la resolución de origen crea una secuencia de bytes para el archivo desde el que el origen de medios lee el contenido de ASF. Para que las conversiones de tiempo sean correctas, la secuencia de bytes asociada al archivo ASF debe tener funcionalidades de búsqueda; De lo contrario, la aplicación obtiene el \_ error MF E \_ BYTESTREAM NOT \_ \_ SEEKABLE de la llamada a **Begin....** Otro requisito para las conversiones de tiempo es que el archivo ASF, representado por el origen de medios de ASF, debe tener objetos de índice de ASF. Los tiempos de presentación y los códigos de tiempo se extraen de los objetos de índice de ASF que mantienen todos los índices y los puntos de búsqueda correspondientes para el archivo ASF. Para la traducción de código de tiempo a tiempo de presentación, el archivo ASF debe contener un objeto de índice simple; para la traducción de tiempo de código a presentación, el archivo ASF debe tener un objeto Index. Las operaciones de conversión se basan en el *indexador* subyacente (componente WMContainer) para analizar y leer el objeto index asociado al archivo ASF. Si el archivo no contiene un objeto index, la aplicación recibe de forma asincrónica el código de error MF \_ E \_ NO \_ INDEX.

Para traducir la hora solicitada por la aplicación, el origen multimedia enumera las secuencias dentro del archivo y busca la secuencia que contiene el objeto de índice de ASF adecuado. Si se encuentra este tipo de flujo, el origen multimedia analiza los paquetes asf de la secuencia hasta que se alcanza el código de hora correcto. Una vez que encuentra el ejemplo correcto, recupera el tiempo de presentación correspondiente o el código de hora del ejemplo y lo devuelve al autor de la llamada.

### <a name="script-command-support"></a>Compatibilidad con comandos de script

Al compilar una topología de ASF que contiene un flujo de script, se agrega un nodo secuencia de script a la topología. Este nodo enviará ASAMPLES en el momento adecuado. El elemento IMFSample proporcionado por el nodo de origen del script almacena los datos en EL ELEMENTO IMFMediaBuffer asociado al ejemplo. Puede llamar a CopyToBuffer en el ejemplo para obtener un ELEMENTO IMFMediaBuffer y, a continuación, llamar a Lock en el búfer para obtener los datos. 

Las cargas de secuencias de script se empaquetan en el búfer como una cadena de tipo, seguidas de NULL, seguidas de la cadena de comando, seguidas de NULL. Las cadenas son Unicode en formato ASF.

Por ejemplo, una carga podría ser como la siguiente (donde \0 indica un carácter NULL):

*URL\0http://contoso.com\0*

*Text\0Este es un título\0*



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
