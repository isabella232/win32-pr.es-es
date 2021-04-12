---
description: Al crear un archivo ASF, el objeto ContentInfo debe conocer las características del contenido multimedia para que los distintos objetos de encabezado se rellenen con los valores correctos.
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: Establecer propiedades en el objeto ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e386d5eb33dd1893b195a870425b2336ab9c316f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155320"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>Establecer propiedades en el objeto ContentInfo

Al crear un archivo ASF, el objeto ContentInfo debe conocer las características del contenido multimedia para que los distintos objetos de encabezado se rellenen con los valores correctos.

-   [Configuración relacionada con el contenido en el objeto ContentInfo](#content-related-settings-in-the-contentinfo-object)
-   [Configurar el objeto ContentInfo con la configuración del codificador](#configuring-the-contentinfo-object-with-encoder-settings)
-   [Temas relacionados](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>Configuración relacionada con el contenido en el objeto ContentInfo

Los valores de configuración de contenido son valores de secuencia que se incluyen en el perfil y especifican el identificador de flujo, el tipo de medio y los parámetros de cubo de fugas del receptor de medios. Una vez establecido el perfil en el objeto ContentInfo llamando a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile), estos valores se reflejan en el objeto de encabezado ASF que se generó. Para obtener información acerca de esta configuración, consulte [crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md).

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>Configurar el objeto ContentInfo con la configuración del codificador

Los datos de audio o vídeo de medios digitales son complejos y ocupan grandes cantidades de memoria. En la mayoría de los casos, el audio y el vídeo se comprimen mediante codificadores antes de que se agreguen a un archivo ASF. En Media Foundation, los codificadores se implementan como [transformaciones Media Foundation](media-foundation-transforms.md) (MFTs) con una entrada y una salida. Debe seleccionar el tipo de medio de salida según el tipo de medio del flujo de entrada y el tipo de codificación que elija para comprimir la secuencia.

Antes de la sesión de codificación, el codificador debe configurarse mediante el establecimiento de las propiedades pertinentes según el tipo de codificación.

Después de configurar el codificador, debe configurar el objeto ContentInfo con los valores del codificador porque el [multiplexor ASF](asf-multiplexer.md) y el receptor de medios ASF, que se inicializan con el objeto ContentInfo rellenado, usan valores como los valores del depósito de fugas para generar paquetes de datos ASF. Los valores no se guardan en el objeto de encabezado ASF final. La configuración de codificación se expone como propiedades. Para configurar el objeto ContentInfo con las propiedades del codificador, haga lo siguiente:

1.  Obtener un puntero al almacén de propiedades del codificador consultando directamente el codificador (interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) para la interfaz **IPropertyStore** .
2.  Llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Para establecer las propiedades específicas de la secuencia, especifique el identificador de flujo en el parámetro *wStreamNumber* . en el caso de las propiedades de nivel de archivo, pase 0. El parámetro *ppIStore* recibe un puntero a la interfaz **IPropertyStore** . El almacén de propiedades recibido está vacío.
3.  Llame a **IPropertyStore:: GetValue** en el codificador y obtenga el valor de la propiedad especificando las constantes de clave de propiedad. Para obtener una lista completa de las propiedades de codificación, vea la [referencia de programación de códecs](/previous-versions//aa384554(v=vs.85)).
4.  Llame a **IPropertyStore:: SetValue** en el objeto ContentInfo para establecer la propiedad required en el almacén de propiedades.
5.  Repita los pasos 3 y 4 para cada propiedad que desee establecer.

El receptor de medios ASF se puede crear mediante un objeto de activación mediante una llamada a [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate). El nuevo objeto de receptor de medios se configura en función de la configuración específica del receptor de medios que se puede establecer en el almacén de propiedades del objeto ContentInfo. En la tabla siguiente se muestran las constantes de la propiedad del receptor multimedia ASF.



| Propiedad                                                                                                     | Descripción                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ \_ SENDTIME ASFMEDIASINK base \_**](mfpkey-asfmediasink-base-sendtime-property.md)                   | La hora de envío indica cuándo se liberará la carga dentro del depósito de fugas. Este valor de propiedad indica la primera hora de envío. El multiplexor usa este valor para calcular las horas de envío posteriores para los paquetes generados y garantiza que los datos fluyen de forma permanente a través del depósito de fugas. |
| [**\_velocidad de \_ bits de autoajuste de MFPKEY ASFMEDIASINK \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | Este valor **booleano** indica si el multiplexor debe ajustar la velocidad de bits automáticamente para asegurarse de que los datos no desbordan el depósito de fugas.                                                                                                                                              |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                            | Esto indica la acción de DRM del receptor de medios ASF para la generación de archivos. En esta versión, solo se admite la transcodificación de DRM.                                                                                                                                                                                   |
| [**MFPKEY \_ ASFSTREAMSINK \_ corregido \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | Esta propiedad se debe establecer cuando el codificador decide qué ventana de búfer y velocidad de bits se van a utilizar. Para establecer estos valores, use la interfaz [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) . Debe establecerse para cada secuencia del archivo ASF.                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 
