---
description: Media Foundation proporciona el origen de medios ASF que una aplicación puede utilizar para representar un archivo ASF en el nivel de canalización de la arquitectura.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Origen de medios ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75dc682d48339ce4ff707e7859a6962b9f5cfd92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707570"
---
# <a name="asf-media-source"></a>Origen de medios ASF

Media Foundation proporciona el origen de medios ASF que una aplicación puede utilizar para representar un archivo ASF en el nivel de canalización de la arquitectura.

Para reproducir un archivo ASF, una aplicación puede usar el origen de medios ASF para alimentar datos en una canalización de reproducción. En un escenario de codificación, la aplicación puede usar el origen de medios ASF como origen para convertir en otro formato o para convertir un archivo de velocidad de bits superior en un archivo de velocidad de bits inferior sin cambiar los formatos. El origen de medios ASF debe usarse en la capa de canalización, es decir, una aplicación debe utilizar la sesión multimedia para controlar la operación. Este nivel de acceso permite a las aplicaciones obtener eventos mientras la sesión multimedia está en curso. Para obtener acceso de nivel inferior al contenido ASF, una aplicación debe usar los componentes ASF de la capa WMContainer.

El origen de medios ASF implementa la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , que es la interfaz genérica para orígenes multimedia en Media Foundation. Al igual que cualquier otro origen multimedia, el origen de medios ASF proporciona un descriptor de presentación que describe principalmente el objeto de encabezado ASF. Además, el origen de medios ASF proporciona descriptores de secuencia que representan cada secuencia en el contenido multimedia. Para obtener más información, consulte [ASF File Structure](asf-file-structure.md).

-   [Crear el origen de medios ASF](#creating-the-asf-media-source)
-   [Opciones de configuración para el origen de medios ASF](#configuration-settings-for-the-asf-media-source)
-   [Modelo de objetos de origen de medios ASF](#asf-media-source-object-model)
-   [Servicios de origen de medios ASF](#asf-media-source-services)
    -   [Conversión de código de tiempo](#timecode-translation)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-asf-media-source"></a>Crear el origen de medios ASF

Para crear el origen de medios ASF, la aplicación debe utilizar la [resolución de origen](source-resolver.md). Con el fin de crear el origen de medios ASF, la aplicación debe proporcionar el origen para el que la resolución de origen crea el origen de medios ASF. La información de origen se debe proporcionar especificando la dirección URL del archivo de código fuente o el flujo de bytes que contiene el medio. Si la aplicación decide crear el origen de medios ASF especificando la dirección URL, debe llamar a [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para una operación sincrónica o **IMFSourceResolver:: Begin... EndCreateObjectFromURL** para la operación asincrónica. El proceso para crear el origen de medios a partir de una secuencia de bytes es similar. La aplicación debe llamar a [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) para una operación sincrónica o **IMFSourceResolver:: Begin... EndCreateObjectFromBytestream** para la operación asincrónica. Estas llamadas deben especificar el \_ \_ MEDIASOURCE de resolución MF en el parámetro *dwFlags* . Para obtener más información sobre el uso de esta marca, vea usar el solucionador de origen.

Si la aplicación especifica una dirección URL, para un archivo local, la cadena de dirección URL puede contener la ruta de acceso del archivo multimedia o tener como prefijo el esquema "File:". La extensión de nombre de archivo debe ser ". ASF", ". WM", L ". WMA" o ". WMV". En el caso de un archivo ASF en la red, la resolución de origen crea el [origen de red](network-source-features.md), que usa el origen de medios ASF.

Durante el proceso de creación de objetos, el solucionador de origen busca la lista de controladores de esquema y los controladores de secuencias de bytes en el registro del sistema y carga el controlador coincidente más cercano que puede analizar el contenido multimedia y también crear el objeto de origen multimedia bajo. Independientemente del método utilizado para crear el origen de medios (dirección URL y secuencia de bytes), la resolución de origen crea una secuencia de bytes y lee el contenido de los medios de origen en el flujo de bytes. Para obtener más información, vea [controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Para obtener un ejemplo de código sobre cómo crear un origen de medios, vea [usar el solucionador de origen](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Opciones de configuración para el origen de medios ASF

La resolución de origen consulta las capacidades de la secuencia de bytes subyacente y determina las operaciones que se permiten en el origen multimedia recién creado. Una de estas capacidades es la búsqueda. Si se permite una operación de búsqueda, la aplicación puede especificar el modo de búsqueda que el origen multimedia utiliza mientras busca en un punto determinado de la presentación.

Una aplicación puede establecer el modo de búsqueda para el origen de medios que se va a usar durante la creación del objeto. Una vez creado el origen de medios ASF con el modo de búsqueda especificado, no se puede modificar en el origen de medios ni cambiar dinámicamente durante una presentación. Las preferencias de búsqueda se especifican como propiedades en la llamada de la aplicación a los métodos de resolución de origen pertinentes que se usan para crear el origen de medios. Este conjunto de propiedades se establece en un almacén de propiedades y se pasa al parámetro *pProps* . Si no se pasan estas propiedades, el origen multimedia funciona con la configuración predeterminada. Para obtener más información acerca de cómo establecer estas propiedades, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Si se permite la búsqueda, el origen de medios ASF admite los siguientes modos de búsqueda:

-   Búsqueda exacta: en este modo, el origen de medios ASF se basa en el objeto de índice ASF del archivo ASF. Si el archivo no tiene el objeto de índice, la búsqueda exacta se deshabilita y se usa uno de los otros modos en función de las propiedades especificadas por la aplicación que se establecen en el origen del medio.
-   Búsqueda aproximada: este modo lo solicita la aplicación pasando [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) en el almacén de propiedades a los métodos de resolución de origen pertinentes. Sin embargo, la búsqueda aproximada solo se utiliza si la secuencia de bytes no admite búsquedas basadas en el tiempo. En este modo, el origen de medios determina una hora de inicio que está relativamente más cercana al tiempo de búsqueda. Si el archivo ASF contiene un objeto de índice ASF, se usa para calcular la hora de inicio. La búsqueda aproximada es menos precisa pero más rápida que la búsqueda exacta porque el tiempo necesario para representar la primera muestra en la hora de inicio predeterminada es más rápido.
-   Búsqueda iterativa: para establecer este modo, la aplicación debe establecer la [propiedad \_ \_ IterativeSeekIfNoIndex de ASFMediaSource de MFPKEY](mfpkey-asfmediasource-iterativeseekifnoindex.md) . La búsqueda iterativa es un algoritmo para encontrar una posición en un archivo ASF que no contiene ningún objeto de índice ASF. En este modo, el origen multimedia determina una estimación aproximada del punto de búsqueda mediante la lectura del desplazamiento del flujo de bytes. Usa una serie de aproximaciones, en función de la velocidad de bits media, para que se acerquen progresivamente al tiempo de búsqueda del destino. (El algoritmo es similar a una búsqueda binaria). La búsqueda iterativa puede tardar más que la búsqueda mediante el uso del objeto de índice, por lo que está deshabilitada de forma predeterminada. Si establece esta propiedad, use las siguientes propiedades para establecer los parámetros de búsqueda: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ en \_ milisegundos](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Estas propiedades establecen el número máximo de iteraciones y la tolerancia, respectivamente. El algoritmo se detiene cuando alcanza el número máximo de iteraciones o cuando encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada.

En pocas palabras, la aplicación tiene la opción de elegir búsqueda aproximada o iterativa cuando el archivo ASF no contiene un objeto de índice ASF.

## <a name="asf-media-source-object-model"></a>Modelo de objetos de origen de medios ASF

El origen de medios ASF implementa la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) y expone las siguientes interfaces. Una aplicación puede obtener una referencia a estas interfaces mediante una llamada a **IMFMediaSource:: QueryInterface** en el origen multimedia ASF.



| Interfaz                                                | Descripción                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Se requiere para todos los orígenes multimedia.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Se requiere para todos los orígenes multimedia. Permite a las aplicaciones obtener eventos del origen multimedia a través de la sesión multimedia.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Consulta el origen de medios para la interfaz de servicio especificada.                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Establece y obtiene propiedades en el origen de los medios. Cada propiedad contiene un nombre descriptivo y un valor.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Describe los metadatos del archivo ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Recupera una colección de metadatos, ya sea para una presentación completa o para un flujo en la presentación.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Consulta el intervalo de velocidades de reproducción que se admiten, incluida la reproducción inversa.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Obtiene o establece la velocidad de reproducción.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Obtiene la ITA para cada una de las secuencias ASF contenidas en el origen.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Permite a un origen de medios recibir un puntero a la interfaz [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , que se usa para crear objetos en el proceso de PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Convierte entre la sociedad de códigos de tiempo de imágenes de movimiento y de ingeniería de televisión (SMPTE) y las unidades de tiempo de 100-nanosegundos.                              |



 

## <a name="asf-media-source-services"></a>Servicios de origen de medios ASF

El origen de medios ASF proporciona varios servicios que se limitan al ámbito del archivo ASF. Para obtener un puntero a un servicio determinado, la aplicación debe usar uno de los siguientes identificadores de servicio en su llamada a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Para obtener más información, consulte [interfaces de servicio](service-interfaces.md).



| Identificador de servicio               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_servicio de \_ control de tasa MF \_       | Con este identificador, una aplicación puede obtener un puntero a las interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) o [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . Mediante el uso del objeto de compatibilidad de tarifas implementado por el origen de medios, la aplicación puede comprobar si la tasa determinada es compatible con el archivo multimedia ASF subyacente y la velocidad más lenta. Mediante el uso del objeto de control de velocidad, la aplicación puede obtener y establecer la velocidad de reproducción. Si la aplicación especifica una tasa determinada para la reproducción, el origen de medios ASF comprueba primero si la tasa solicitada está dentro de los límites de frecuencia (determinada por las tarifas más rápidas y lentas) y, a continuación, establece la velocidad. Esto no comprueba las condiciones variables, ya que la velocidad de bits podría cambiar en cualquier momento según el ancho de banda de red. Para obtener más información, [evalúe el control](rate-control.md). |
| \_servicio de proveedor de metadatos MF \_ \_  | Con este identificador, la aplicación puede obtener un puntero a la interfaz [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) del origen multimedia ASF. Esta interfaz proporciona acceso a información sobre el archivo ASF específicamente los objetos de encabezado ASF y las secuencias contenidas en el contenido multimedia. La información del encabezado se expone a través de los atributos del descriptor de presentación y la información del flujo se proporciona a través de los atributos de descripto Para obtener más información acerca de estos atributos, consulte [atributos de Media Foundation para los objetos de encabezado ASF](media-foundation-attributes-for-asf-header-objects.md). Además de la información que se expone a través de atributos, también existen metadatos descriptivos, que se establecen como propiedades.                                                                                                 |
| \_servicio de \_ controlador de propiedades MF \_   | Con este identificador, la aplicación puede obtener un puntero a la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) del origen multimedia ASF. El almacén de propiedades contiene todos los metadatos relacionados con el archivo ASF. Este identificador es nuevo en Windows 7 y reemplaza el \_ \_ servicio del proveedor de metadatos MF \_ para obtener propiedades de metadatos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| MFNETSOURCE \_ Statistics \_ Service | Para obtener más información, consulte recuperar estadísticas de red en el [registro de cliente](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_servicio de código de tiempo MF \_            | Mediante este identificador, la aplicación puede obtener un puntero a la interfaz [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) del origen del medio. Esta implementación se puede usar para realizar traducciones de código de tiempo, como la conversión de código de tiempo SMPTE a unidades 100-nanosegundos y viceversa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Conversión de código de tiempo

El origen de medios ASF proporciona un servicio de traducción de código de tiempo que permite a la aplicación convertir el código de tiempo SMPTE al tiempo de presentación más cercano (en una unidad de 100 segundos). Por el contrario, la aplicación también puede obtener el código de tiempo para una hora de presentación solicitada. El servicio está disponible a través de la interfaz [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) , que implementa el origen multimedia ASF. Las llamadas al método en este puntero de interfaz son asincrónicas que se pueden ejecutar desde el subproceso de aplicación principal sin bloquear la interfaz de usuario de la aplicación.

En los pasos siguientes se resume el procedimiento para la traducción del código de tiempo:

1.  Obtiene un puntero a la interfaz [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) del origen multimedia ASF llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y especificando el identificador del **servicio de código de \_ tiempo \_ MF** .
2.  Llame a [**IMFTimecodeTranslate:: BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) o [**IMFTimecodeTranslate:: BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) y especifique la hora que se va a traducir. En el caso de **BeginConvertTimecodeToHNS** , el código de tiempo debe especificarse como una variable [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) con el tipo de datos **VT \_ i8** . El método **BeginConvertHNSToTimecode** requiere el tiempo en unidades de 100-nanosegundos como tipo de [**MFTIME**](mftime.md) .
3.  Complete la operación asincrónica mediante una llamada a [**IMFTimecodeTranslate:: EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) o **IMFTimecodeTranslate:: EndConvertTimecodeToHNS** adecuadamente.

Durante la creación del origen multimedia, la resolución de origen crea una secuencia de bytes para el archivo desde el que el origen multimedia lee el contenido ASF. Para que las conversiones de tiempo se realicen correctamente, el flujo de bytes asociado al archivo ASF debe tener capacidades de búsqueda. de lo contrario, la aplicación obtiene \_ el \_ \_ error BYTESTREAM no \_ buscable en la llamada a **Begin...** . Otro requisito para las conversiones de tiempo es que el archivo ASF, representado por el origen de medios ASF, debe tener objetos de índice ASF. Los tiempos de presentación y los códigos de tiempo se extraen de los objetos de índice ASF que mantienen todos los índices y los puntos de búsqueda correspondientes del archivo ASF. Para la traducción de código de tiempo a tiempo de presentación, el archivo ASF debe contener un objeto de índice simple. para la traducción de tiempo de código a presentación, el archivo ASF debe tener un objeto de índice. Las operaciones de conversión dependen del *indexador* subyacente (componente WMContainer) para analizar y leer el objeto de índice asociado al archivo ASF. Si el archivo no contiene un objeto de índice, la aplicación recibe de forma asincrónica el \_ código de error MF E \_ no \_ index.

Para traducir el tiempo solicitado por la aplicación, el origen multimedia enumera las secuencias del archivo y busca la secuencia que contiene el objeto de índice ASF adecuado. Si se encuentra este tipo de flujo, el origen multimedia analiza los paquetes ASF de la secuencia que se analizan hasta que se alcanza el código de tiempo correcto. Después de encontrar el ejemplo correcto, recupera la hora de presentación correspondiente o el código de tiempo del ejemplo y lo devuelve al autor de la llamada.

### <a name="script-command-support"></a>Compatibilidad con comandos de script

Al compilar una topología ASF que contiene una secuencia de script, se agrega un nodo de secuencia de script a la topología. Este nodo enviará IMFSamples en el momento adecuado. El IMFSample proporcionado por el nodo de origen del script almacena los datos en el IMFMediaBuffer asociado con el ejemplo. Puede llamar a CopyToBuffer en el ejemplo para obtener un IMFMediaBuffer y, a continuación, llamar a Lock en el búfer para obtener los datos. 

Las cargas de script de secuencia se empaquetan en el búfer como una cadena de tipo, seguida de NULL, seguido de la cadena de comandos, seguida de NULL. Las cadenas son Unicode en formato ASF.

Por ejemplo, una carga podría ser similar a la siguiente (donde \ 0 indica un carácter nulo):

*URL\0http://contoso.com\0*

*Text\0This es un caption\0*



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
