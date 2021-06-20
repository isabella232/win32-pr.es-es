---
description: Obtenga información sobre cómo establecer propiedades en el receptor de archivos ASF, que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Establecer propiedades en el receptor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b6b000ed04c7858251f7388d3edc6a40e0b213
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407518"
---
# <a name="setting-properties-in-the-file-sink"></a>Establecer propiedades en el receptor de archivos

El receptor de archivos DE ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores multimedia de ASF.](asf-media-sinks.md)

Después [de crear el receptor de archivos ASF,](creating-the-asf-file-sink.md)debe configurarse con información sobre los flujos del archivo de salida. Este procedimiento se describe en [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md). Puede establecer propiedades adicionales en el receptor de archivos en función del tipo de codificación; cubos con pérdidas; propiedades generales del archivo. Esta configuración no se escribe en el objeto de encabezado asf final. En este tema se describe el proceso de agregar estas propiedades en el almacén de propiedades del receptor de archivos.

El objeto ContentInfo mantiene las propiedades de archivo global y las propiedades de secuencia individuales para el receptor de archivos. Para obtener información sobre cómo obtener una referencia al objeto ContentInfo de ASF del receptor de archivos, vea [Creating the ASF File Sink](creating-the-asf-file-sink.md).

Para obtener una referencia al almacén de propiedades del receptor de archivos ([**IPropertyStore),**](/windows/win32/api/propsys/nn-propsys-ipropertystore)llame a [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en la referencia del objeto ContentInfo del receptor de archivos.

## <a name="stream-encoding-properties"></a>Propiedades de codificación de secuencias

Para codificar el contenido correctamente, el archivo debe conocer cierta información de codificación, como el tipo de codificación y los parámetros de codificación relacionados. Estos valores se establecen en el receptor de archivos como valores de propiedad en un almacén de propiedades que mantiene el objeto ContentInfo de ASF. Si va a configurar el receptor de archivos antes de crear instancias de los codificadores pertinentes, puede usar el objeto ContentInfo con todas las propiedades rellenadas para crear los codificadores de Windows Media. En este caso, las propiedades se establecen automáticamente en los codificadores con instancias. Por el contrario, si va a crear los codificadores antes del receptor, asegúrese de que las propiedades establecidas en los codificadores se copian en el almacén de propiedades del receptor de archivos.

Para establecer las propiedades de codificación, necesita acceso al almacén de propiedades de nivel de secuencia del receptor de archivos. Pase el número de secuencia en el *parámetro wStreamNumber* del método [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) Los números de secuencia deben coincidir con los valores establecidos al configurar cada secuencia en el perfil. Los valores de propiedad se establecen mediante una [**llamada a IPropertyStore::SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). En la tabla siguiente se describen las propiedades admitidas.

Las propiedades dependen del tipo de codificación. Para obtener información sobre las propiedades y los valores respectivos que debe establecer, vea [Propiedades de codificación](configuring-the-encoder.md).

## <a name="leaky-bucket-property"></a>Propiedad leaky bucket

Los parámetros de depósito con pérdida determinan la ventana de búfer real que usa el codificador para la secuencia. La propiedad [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del receptor de archivos contiene los parámetros del depósito de pérdidas, la velocidad de bits, la ventana de búfer y la integridad inicial del búfer. Esta propiedad se establece en el almacén de propiedades de nivel de secuencia para el receptor de archivos y debe establecerse una vez creados y configurados los codificadores. Este valor se establece en . Durante la negociación del tipo de medio, el codificador decide la ventana de búfer y la velocidad de bits que se usará. Puede obtener estos valores mediante la interfaz **IWMCodecLeakyBucket,** que se define en wmcodecifaces.h y debe vincular a wmcodecdspuuid.lib para llamar a sus métodos.

Los valores recuperados se pueden establecer para esta propiedad para cada secuencia del receptor de archivos ASF.

## <a name="global-file-sink-properties"></a>Propiedades del receptor global de archivos

Para obtener el almacén de propiedades global del receptor de archivos, pase 0 en el parámetro *wStreamNumber* del método [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) Los valores de propiedad se establecen mediante una [**llamada a IPropertyStore::SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). En la tabla siguiente se describen las propiedades admitidas.

| Propiedades de nivel de archivo                                                                                | Descripción                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)           | El tiempo de envío indica cuándo se liberará la carga dentro del depósito de pérdidas. Este valor de propiedad indica la primera hora de envío. El multiplexor usa este valor para calcular los tiempos de envío subsiguientes de los paquetes generados y garantiza que los datos fluyen constantemente a través del cubo de pérdidas. |
| [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Este valor BOOL indica si el multiplexor debe ajustar la velocidad de bits automáticamente para asegurarse de que los datos no desbordan el cubo con pérdidas.                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | Esto indica la acción DRM del receptor de medios de ASF para la generación de archivos. En esta versión, solo se admite la transcodificación DRM.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores multimedia de ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
