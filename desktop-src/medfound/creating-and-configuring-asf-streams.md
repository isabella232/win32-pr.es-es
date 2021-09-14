---
description: Cada archivo ASF contiene una o varias secuencias. El objeto ASF Profile representa una colección de secuencias de ASF. Para la codificación ASF, debe crear y configurar las secuencias que desea codificar.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Creación y configuración de asf Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eabce588022dd66947f34e4dcd9db61f26448b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252500"
---
# <a name="creating-and-configuring-asf-streams"></a>Creación y configuración de asf Secuencias

Cada archivo ASF contiene una o varias secuencias. El [objeto ASF Profile](asf-profile.md) representa una colección de secuencias de ASF. Para la codificación ASF, debe crear y configurar las secuencias que desea codificar.

Una aplicación puede realizar las siguientes tareas con el objeto de perfil de ASF:

-   Agregar o quitar una secuencia.
-   Obtenga los valores de configuración de un flujo.
-   Configure las extensiones de carga.
-   Agregue, quite o modifique un objeto de exclusión mutua de ASF.

En este tema se incluyen las siguientes secciones.

-   [Creación de una nueva secuencia](#creating-a-new-stream)
-   [Asignación de números de secuencia](#assigning-stream-numbers)
-   [Establecimiento de valores de cubo de pérdida](#setting-leaky-bucket-values)
-   [Extensiones de carga](#payload-extensions)
-   [Agregar una secuencia al perfil](#adding-a-stream-to-the-profile)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-new-stream"></a>Creación de una nueva secuencia

Un objeto de perfil de ASF debe contener valores de configuración para al menos una secuencia de ASF. Cada secuencia se representa mediante un *objeto de configuración* de flujo, que expone la interfaz [**DEFStreamConfig DE LAFF.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) La información del objeto de configuración de flujo corresponde al objeto de propiedades de secuencia y a los objetos de propiedades de secuencia extendidas en el encabezado de archivo ASF. (Vea [ASF File Structure [Estructura de archivos ASF]).](asf-file-structure.md)

Para agregar una secuencia a un perfil de ASF, realice los pasos siguientes:

1.  Cree un objeto de configuración de flujo de flujo vacío.
2.  Configure la secuencia según los requisitos de la aplicación.
3.  Agregue la secuencia al perfil.

Para crear una secuencia para el perfil, llame a [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para crear un objeto de configuración de flujo vacío y recibir el puntero en el *parámetro ppIStream.* **CreateStream** debe conocer el tipo de secuencia que se debe crear. Los tipos más comunes de secuencias que se usan en los archivos ASF son las secuencias de audio y vídeo. En Media Foundation, el objeto de tipo de medio que expone la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) indica los tipos de secuencia. El tipo principal del tipo de medio define la categoría de la secuencia multimedia digital, como audio o vídeo. El subtipo define el formato del tipo principal. El tipo de medio inicial establecido **por CreateStream** se puede cambiar mediante el objeto de configuración de flujo. Para recuperar el tipo de medio para la secuencia, llame a [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) o para recuperar la llamada de tipo principal [**a IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype). El tipo de medio inicial de una secuencia se puede reemplazar por un nuevo tipo de medio configurado mediante una llamada a [**IMFASFStreamConfig::SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype).

Si una aplicación crea un perfil a partir de un descriptor de presentación válido mediante una llamada a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). La función establece automáticamente los objetos de configuración de flujo para cada una de las secuencias y los establece en el perfil. Los tipos de medios de secuencia se establecen en función de los descriptores de flujo asociados al descriptor de presentación.

## <a name="assigning-stream-numbers"></a>Asignación de números de secuencia

Secuencias de todos los tipos deben tener asignado un número de secuencia. Los números de secuencia no deben ser secuenciales, pero deben estar en el intervalo de 1 a 127. Para asignar números de flujo, llame [**a IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Para obtener la llamada de número de secuencia, [**IMFASFStreamConfig::GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Un número de flujo es diferente de un índice de secuencia, que se usa al obtener secuencias en un perfil mediante EL USO DE [**LAPERFISFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream). El índice de secuencia es un número asignado a la secuencia por el objeto de perfil. Los índices de secuencia oscilan entre 0 y uno menos que el número de secuencias recuperadas por [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount). También puede obtener una secuencia del perfil por número de secuencia llamando a [**IMFASFProfile::GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber).

 

## <a name="setting-leaky-bucket-values"></a>Establecimiento de valores de cubo de pérdida

Cada objeto de configuración de flujo que representa una secuencia debe tener asociados parámetros de cubo de pérdida, velocidad de bits y valores de ventana de búfer.

Estos valores están disponibles para la aplicación mediante el atributo [**\_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) y el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2.**](mf-asfstreamconfig-leakybucket2-attribute.md) Para la codificación de archivos, los valores reales dependen del tipo de codificación y los decide el codificador. Si ya tiene un codificador configurado y el tipo de salida está establecido en el codificador, la aplicación debe consultar los parámetros del cubo de pérdidas y establecer los valores de estos atributos.

Si usa los componentes de la capa de canalización y configura las secuencias para el receptor de medios de ASF, lo más probable es que no tenga un codificador configurado. En este caso, debe consultar las negociaciones de tipo multimedia posteriores al codificador y establecer el valor actualizado en la propiedad [**\_ MFPKEY ASFSTREAMSINK \_ \_ CORRECTED LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del almacén de propiedades del receptor de medios de ASF. El almacén de propiedades de codificación se recupera a través del objeto ContentInfo asociado al perfil. Los valores actualizados se reflejan automáticamente en los valores de atributo de cubo de pérdida de la secuencia. Para obtener información general sobre los cubos con fugas y cómo obtener el valor del cubo de fugas del codificador, consulte [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).

## <a name="payload-extensions"></a>Extensiones de carga

Los datos multimedia de las secuencias se agregan [](media-samples.md) al objeto de datos de ASF como ejemplos multimedia mediante el [multiplexador de ASF.](asf-multiplexer.md) Estos ejemplos multimedia pueden contener datos de extensión de carga: datos de código de tiempo de SMPTE, relación de aspecto de píxeles no cuadrados, duración de la muestra y, si el ejemplo los contiene, un fotograma clave de vídeo. Para obtener una lista de los tipos de extensión de carga [admitidos, vea ASF Payload Extension GUIDs (GUID de extensión de carga de ASF).](asf-payload-extension-guids.md)

Una secuencia debe configurarse para aceptar la extensión de carga para que durante la generación de muestras el multiplexador pueda agregar los datos adicionales a cada muestra para esa secuencia.

Para obtener el número total de extensiones de carga establecidas en la secuencia, llame a [**IMFASFStreamConfig::GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) y, a continuación, enumere la lista mediante una llamada a [**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension). Para agregar la extensión de carga para la secuencia, llame [**a IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). Esto agregará datos adicionales a los ejemplos de medios individuales generados para la secuencia.

Para quitar las extensiones de carga existentes asociadas a la secuencia, llame a [**IMFASFStreamConfig::RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions).

## <a name="adding-a-stream-to-the-profile"></a>Agregar una secuencia al perfil

Una vez configurada una secuencia, llame a [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para agregar la secuencia al perfil.

Para quitar una secuencia existente en el perfil, llame [**a IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

El perfil configurado debe establecerse en el objeto ContentInfo llamando a [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Si realiza cambios en una secuencia existente, debe agregarla de nuevo al perfil y establecer el perfil en el objeto ContentInfo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfil de ASF](asf-profile.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



