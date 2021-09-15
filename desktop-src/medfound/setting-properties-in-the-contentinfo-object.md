---
description: Al crear un archivo ASF, el objeto ContentInfo debe conocer las características del contenido multimedia para que los distintos objetos de encabezado se rellenen con los valores correctos.
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: Establecer propiedades en el objeto ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e386d5eb33dd1893b195a870425b2336ab9c316f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574789"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>Establecer propiedades en el objeto ContentInfo

Al crear un archivo ASF, el objeto ContentInfo debe conocer las características del contenido multimedia para que los distintos objetos de encabezado se rellenen con los valores correctos.

-   [Contenido relacionado Configuración en el objeto ContentInfo](#content-related-settings-in-the-contentinfo-object)
-   [Configuración del objeto ContentInfo con el codificador Configuración](#configuring-the-contentinfo-object-with-encoder-settings)
-   [Temas relacionados](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>Contenido relacionado Configuración en el objeto ContentInfo

Las opciones de configuración de contenido son las opciones de secuencia, que se encuentran dentro del perfil y especifican el identificador de flujo, el tipo de medio y los parámetros del cubo de pérdidas para el receptor de medios. Después de establecer el perfil en el objeto ContentInfo mediante una llamada a [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile), estos valores se reflejan en el objeto de encabezado ASF que se generó. Para obtener información sobre estas opciones, vea [Creating and Configuring ASF Secuencias](creating-and-configuring-asf-streams.md).

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>Configuración del objeto ContentInfo con el codificador Configuración

Los datos de audio o vídeo multimedia digitales son complejos y ocupa grandes cantidades de memoria. En la mayoría de las circunstancias, tanto el audio como el vídeo se comprimen mediante codificadores antes de agregarse a un archivo ASF. En Media Foundation, los codificadores se implementan [como transformaciones](media-foundation-transforms.md) de Media Foundation (MTA) con una entrada y una salida. Debe seleccionar el tipo de medio de salida según el tipo de medio del flujo de entrada y el tipo de codificación que elija para comprimir la secuencia.

Antes de la sesión de codificación, el codificador debe configurarse estableciendo las propiedades pertinentes en función del tipo de codificación.

Después de configurar el codificador, debe configurar el objeto ContentInfo con los valores del codificador porque el [multiplexor de ASF](asf-multiplexer.md) y el receptor de medios de ASF, que se inicializan con el objeto ContentInfo rellenado, usan valores como los valores del cubo de fugas para generar paquetes de datos de ASF. Los valores no se guardan en el objeto de encabezado asf final. La configuración de codificación se expone como propiedades. Para configurar el objeto ContentInfo con las propiedades del codificador, haga lo siguiente:

1.  Obtenga un puntero al almacén de propiedades del codificador consultando el codificador (interfaz [**DETRANSFORMTRANSFORM)**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) directamente para la **interfaz IPropertyStore.**
2.  Llame [**a IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Para establecer propiedades específicas de la secuencia, especifique el identificador de flujo en el *parámetro wStreamNumber;* para las propiedades de nivel de archivo, pase 0. El *parámetro ppIStore* recibe un puntero a la **interfaz IPropertyStore.** El almacén de propiedades recibido está vacío.
3.  Llame **a IPropertyStore::GetValue** en el codificador y obtenga el valor de propiedad especificando las constantes de clave de propiedad. Para obtener una lista completa de las propiedades de codificación, vea [la Referencia de programación de códecs](/previous-versions//aa384554(v=vs.85)).
4.  Llame **a IPropertyStore::SetValue en** el objeto ContentInfo para establecer la propiedad necesaria en el almacén de propiedades.
5.  Repita los pasos 3 y 4 para cada propiedad que quiera establecer.

El receptor de medios de ASF se puede crear mediante un objeto de activación llamando a [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate). El nuevo objeto receptor multimedia se configura en función de la configuración específica del receptor multimedia que se puede establecer en el almacén de propiedades del objeto ContentInfo. En la tabla siguiente se muestran las constantes de propiedad de receptor de medios de ASF.



| Propiedad                                                                                                     | Descripción                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)                   | El tiempo de envío indica cuándo se liberará la carga dentro del depósito de pérdidas. Este valor de propiedad indica la primera hora de envío. El multiplexor usa este valor para calcular los tiempos de envío subsiguientes de los paquetes generados y garantiza que los datos fluyen constantemente a través del cubo de pérdidas. |
| [**VELOCIDAD DE BITS DE AJUSTE AUTOMÁTICO \_ DE MFPKEY ASFMEDIASINK \_ \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | Este **valor BOOL** indica si el multiplexor debe ajustar la velocidad de bits automáticamente para asegurarse de que los datos no desbordan el cubo de fugas.                                                                                                                                              |
| [**DRMACTION \_ DE ASFMEDIASINK DE MFPKEY \_**](mfpkey-asfmediasink-drmaction-property.md)                            | Esto indica la acción DRM del receptor de medios de ASF para la generación de archivos. En esta versión, solo se admite la transcodificación DRM.                                                                                                                                                                                   |
| [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | Esta propiedad debe establecerse cuando el codificador decida qué ventana de búfer y velocidad de bits usar. Para establecer estos valores, use la [**interfaz IWMCodecLeakyBucket.**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) Debe establecerse para cada secuencia del archivo ASF.                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 
