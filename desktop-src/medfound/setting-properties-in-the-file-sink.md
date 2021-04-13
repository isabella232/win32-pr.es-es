---
description: El receptor de archivos ASF es una implementación de IMFMediaSink proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios ASF y el uso general, consulte receptores multimedia ASF.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Establecer propiedades en el receptor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30af39cf13e88f6edf2a6ab68caac27c2400955a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360479"
---
# <a name="setting-properties-in-the-file-sink"></a>Establecer propiedades en el receptor de archivos

El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos y el uso general de los receptores de medios ASF, consulte [receptores de medios ASF](asf-media-sinks.md).

Después de [crear el receptor de archivos ASF](creating-the-asf-file-sink.md), debe configurarse con información sobre las secuencias del archivo de salida. Este procedimiento se describe en [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md). Puede establecer propiedades adicionales en el receptor de archivos según el tipo de codificación; depósitos con fugas; propiedades generales del archivo. Estos valores no se escriben en el objeto de encabezado ASF final. En este tema se describe el proceso de agregar estas propiedades en el almacén de propiedades del receptor de archivos.

El objeto ContentInfo mantiene las propiedades de archivo globales y las propiedades de flujo individuales del receptor de archivos. Para obtener información sobre cómo obtener una referencia al objeto ContentInfo ASF del receptor de archivo, consulte [crear el receptor de archivos ASF](creating-the-asf-file-sink.md).

Para obtener una referencia al almacén de propiedades del receptor de archivo ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)), llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en la referencia del objeto ContentInfo del receptor de archivo.

## <a name="stream-encoding-properties"></a>Propiedades de codificación de secuencias

Para codificar el contenido correctamente, el archivo necesita conocer cierta información de codificación, como el tipo de codificación y los parámetros de codificación relacionados. Estos valores se establecen en el receptor de archivo como valores de propiedad en un almacén de propiedades mantenido por el objeto ContentInfo ASF. Si está configurando el receptor de archivo antes de crear una instancia de los codificadores pertinentes, puede usar el objeto ContentInfo con todas las propiedades rellenas para crear los codificadores de Windows Media. En este caso, las propiedades se establecen automáticamente en los codificadores con instancias. Por el contrario, si va a crear los codificadores antes del receptor, asegúrese de que las propiedades establecidas en los codificadores se copian en el almacén de propiedades del receptor de archivo.

Para establecer las propiedades de codificación, necesita tener acceso al almacén de propiedades de nivel de secuencia del receptor de archivos. Pase el número de secuencia en el parámetro *wStreamNumber* del método [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . Los números de secuencia deben coincidir con los valores establecidos al configurar cada secuencia en el perfil. Los valores de propiedad se establecen mediante una llamada a [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). En la tabla siguiente se describen las propiedades admitidas.

Las propiedades dependen del tipo de codificación. Para obtener información sobre las propiedades y los valores respectivos que debe establecer, consulte [propiedades de codificación](configuring-the-encoder.md).

## <a name="leaky-bucket-property"></a>Propiedad de depósito de fugas

Los parámetros de depósito con fugas determinan la ventana de búfer real utilizada por el codificador para la secuencia. La propiedad [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corregida \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del receptor de archivo contiene los parámetros de depósito con fugas, la velocidad de bits, la ventana de búfer y el llenado inicial del búfer. Esta propiedad se establece en el almacén de propiedades de propiedad de nivel de secuencia para el receptor de archivos y debe establecerse una vez que se han creado y configurado los codificadores. Este valor se establece en. Durante la negociación del tipo de medio, el codificador decide la ventana del búfer y la velocidad de bits que se va a utilizar. Puede obtener estos valores mediante la interfaz **IWMCodecLeakyBucket** , que se define en wmcodecifaces. h y debe vincular a wmcodecdspuuid. lib para llamar a sus métodos.

Los valores recuperados se pueden establecer para esta propiedad para cada flujo del receptor de archivos ASF.

## <a name="global-file-sink-properties"></a>Propiedades globales del receptor de archivos

Para obtener el almacén de propiedades global del receptor de archivo, pase 0 en el parámetro *wStreamNumber* del método [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . Los valores de propiedad se establecen mediante una llamada a [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). En la tabla siguiente se describen las propiedades admitidas.

| Propiedades de nivel de archivo                                                                                | Descripción                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ \_ SENDTIME ASFMEDIASINK base \_**](mfpkey-asfmediasink-base-sendtime-property.md)           | La hora de envío indica cuándo se liberará la carga dentro del depósito de fugas. Este valor de propiedad indica la primera hora de envío. El multiplexor usa este valor para calcular las horas de envío posteriores para los paquetes generados y garantiza que los datos fluyen de forma permanente a través del depósito de fugas. |
| [**\_velocidad de \_ bits de autoajuste de MFPKEY ASFMEDIASINK \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Este valor BOOLEANO indica si el multiplexor debe ajustar la velocidad de bits automáticamente para asegurarse de que los datos no desbordan el depósito de fugas.                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | Esto indica la acción de DRM del receptor de medios ASF para la generación de archivos. En esta versión, solo se admite la transcodificación de DRM.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores de medios ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
