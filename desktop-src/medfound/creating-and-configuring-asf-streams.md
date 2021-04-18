---
description: Cada archivo ASF contiene una o más secuencias. El objeto de perfil ASF representa una colección de secuencias ASF. En el caso de la codificación ASF, debe crear y configurar las secuencias que desea codificar.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Crear y configurar secuencias ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eabce588022dd66947f34e4dcd9db61f26448b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659785"
---
# <a name="creating-and-configuring-asf-streams"></a>Crear y configurar secuencias ASF

Cada archivo ASF contiene una o más secuencias. El objeto de [perfil ASF](asf-profile.md) representa una colección de secuencias ASF. En el caso de la codificación ASF, debe crear y configurar las secuencias que desea codificar.

Una aplicación puede realizar las tareas siguientes con el objeto de perfil ASF:

-   Agregue o quite un flujo.
-   Obtenga los valores de configuración de una secuencia.
-   Configurar extensiones de carga.
-   Agregar, quitar o modificar un objeto de exclusión mutua de ASF.

En este tema se incluyen las siguientes secciones.

-   [Crear una nueva secuencia](#creating-a-new-stream)
-   [Asignación de números de secuencia](#assigning-stream-numbers)
-   [Establecimiento de valores de cubo con fugas](#setting-leaky-bucket-values)
-   [Extensiones de carga](#payload-extensions)
-   [Agregar una secuencia al perfil](#adding-a-stream-to-the-profile)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-new-stream"></a>Crear una nueva secuencia

Un objeto de perfil ASF debe contener valores de configuración para al menos una secuencia ASF. Cada secuencia se representa mediante un objeto de configuración de la *secuencia* , que expone la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . La información del objeto de configuración de la secuencia se corresponde con el objeto de propiedades de secuencia y los objetos de propiedades de secuencia extendida en el encabezado de archivo ASF. (Vea [estructura de archivos ASF](asf-file-structure.md)).

Para agregar una secuencia a un perfil ASF, realice los pasos siguientes:

1.  Cree un objeto de configuración de secuencia de secuencia vacía.
2.  Configure el flujo según los requisitos de la aplicación.
3.  Agregue la secuencia al perfil.

Para crear una secuencia para el perfil, llame a [**IMFASFProfile:: CreateStream (**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para crear un objeto de configuración de secuencia vacío y recibir el puntero en el parámetro *ppIStream* . **CreateStream (** debe conocer el tipo de la secuencia que se va a crear. Los tipos de secuencias más comunes que se usan en los archivos ASF son las secuencias de audio y vídeo. En Media Foundation, los tipos de flujo se indican mediante el objeto de tipo de medio que expone la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . El tipo principal del tipo de medio define la categoría de la secuencia de medios digitales, como audio o vídeo. El subtipo define el formato del tipo principal. El tipo de medio inicial establecido por **CreateStream (** se puede cambiar mediante el objeto de configuración de vapor. Para recuperar el tipo de medio para la secuencia, llame a [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) o para recuperar la llamada de tipo principal [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype). El tipo de medio inicial de una secuencia se puede reemplazar por un nuevo tipo de medio configurado mediante una llamada a [**IMFASFStreamConfig:: SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype).

Si una aplicación crea un perfil a partir de un descriptor de presentación válido mediante una llamada a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). La función establece automáticamente los objetos de configuración de la secuencia para cada una de las secuencias y los establece en el perfil. Los tipos de medios de secuencia se establecen en función de los descriptores de flujo asociados con el descriptor de presentación.

## <a name="assigning-stream-numbers"></a>Asignación de números de secuencia

A los flujos de todos los tipos se les debe asignar un número de secuencia. Los números de secuencia no deben ser secuenciales, pero deben estar en el intervalo comprendido entre 1 y 127. Para asignar números de secuencia, llame a [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Para obtener la llamada del número de secuencia, [**IMFASFStreamConfig:: GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Un número de secuencia es diferente de un índice de flujo, que se usa al obtener secuencias en un perfil mediante [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream). El índice de la secuencia es un número asignado a la secuencia por el objeto de perfil. Los índices de secuencia oscilan entre 0 y uno menos que el número de flujos recuperados por [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount). También puede obtener una secuencia desde el perfil por número de secuencia mediante una llamada a [**IMFASFProfile:: GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber).

 

## <a name="setting-leaky-bucket-values"></a>Establecimiento de valores de cubo con fugas

Cada objeto de configuración de secuencia que representa una secuencia debe tener asociados parámetros de depósito de pérdida, velocidad de bits y valores de la ventana de búfer.

Estos valores están disponibles para la aplicación mediante el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) y el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) . Para la codificación de archivos, los valores reales dependen del tipo de codificación y el codificador los decide. Si ya tiene un codificador configurado y el tipo de salida se establece en el codificador, la aplicación debe consultar el codificador para los parámetros del cubo de fugas y establecer los valores de estos atributos.

Si usa los componentes de la capa de canalización y configura las secuencias para el receptor multimedia ASF, lo más probable es que no tenga un codificador configurado. En este caso, debe consultar las negociaciones del tipo posterior al medio del codificador y establecer el valor actualizado en la propiedad [**MFPKEY \_ ASFSTREAMSINK \_ corregida \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del almacén de propiedades del receptor de medios ASF. El almacén de propiedades de codificación se recupera a través del objeto ContentInfo asociado al perfil. Los valores actualizados se reflejan automáticamente en los valores de atributo de depósito de fugas de la secuencia. Para obtener información general sobre los cubos con pérdidas y cómo obtener el valor del depósito de fugas del codificador, consulte el [modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md).

## <a name="payload-extensions"></a>Extensiones de carga

Los datos multimedia de las secuencias se agregan al objeto de datos ASF como [muestras multimedia](media-samples.md) del [multiplexor de ASF](asf-multiplexer.md). Estos ejemplos de medios pueden contener datos de extensión de carga: datos de código de tiempo SMPTE, relación de aspecto de píxeles no cuadrado, duración de la muestra y, si el ejemplo lo contiene, un fotograma clave de vídeo. Para obtener una lista de los tipos de extensión de carga admitidos, consulte [GUID de extensión de carga ASF](asf-payload-extension-guids.md).

Una secuencia debe estar configurada para aceptar la extensión de carga, por lo que durante la generación de ejemplo el multiplexor puede Agregar los datos complementarios a cada ejemplo de la secuencia.

Para obtener el número total de extensiones de carga establecidas en la secuencia, llame a [**IMFASFStreamConfig:: GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) y, a continuación, enumere la lista llamando a [**IMFASFStreamConfig:: GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension). Para agregar la extensión de carga para la secuencia, llame a [**IMFASFStreamConfig:: AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). Esto agregará datos complementarios a los ejemplos de medios individuales generados para la secuencia.

Para quitar las extensiones de carga existente asociadas a la secuencia, llame a [**IMFASFStreamConfig:: RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions).

## <a name="adding-a-stream-to-the-profile"></a>Agregar una secuencia al perfil

Una vez configurada una secuencia, llame a [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para agregar la secuencia al perfil.

Para quitar una secuencia existente en el perfil, llame a [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

El perfil configurado debe establecerse en el objeto ContentInfo llamando a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Si realiza cambios en una secuencia existente, debe volver a agregarla al perfil y establecer el perfil en el objeto ContentInfo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfil ASF](asf-profile.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 



