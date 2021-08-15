---
description: Para convertir archivos multimedia al formato ASF, puede usar Windows codificadores multimedia. Obtenga información sobre el uso de objetos de activación de un codificador.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Usar objetos de activación de codificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24915020c1b888be6a1aeaca1e21af95d11cfc181a5c00a91c8359c3f780fa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972744"
---
# <a name="using-an-encoders-activation-objects"></a>Usar objetos de activación de un codificador

Para convertir archivos multimedia al formato ASF, puede usar Windows codificadores multimedia. Para usar estos codificadores, deben estar registrados en el sistema.

Para obtener información sobre el registro del codificador, vea [Creación de instancias de Un codificador MFT.](instantiating-the-encoder-mft.md)

-   [Usar objetos de activación de un codificador](#using-an-encoders-activation-objects)
-   [Enumeración de codificador en Windows 7 y versiones posteriores](#encoder-enumeration-in-windows-7-and-later)
-   [Temas relacionados](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Usar objetos de activación de un codificador

Como alternativa al uso de la interfaz [**DETRANSFORMtransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de un codificador (descrita en Creación de un codificador mediante [CoCreateInstance),](using-an-encoder-s-imftransform--interface.md)puede crear una instancia del objeto de activación para el codificador. Los objetos de activación facilitan la creación del codificador y Media Foundation proporciona las dos funciones siguientes para este enfoque:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) para crear instancias de Windows codificador de audio Multimedia.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) para crear instancias del Windows de vídeo multimedia.

Ambas funciones requieren que cree el tipo de medio de destino y establezca las propiedades de codificación antes de llamar a estas funciones. Si la aplicación usa componentes de [ASF](pipeline-layer-asf-components.md) de capa de canalización para codificar un archivo en formato ASF y ya ha creado y configurado los receptores de medios de [ASF,](asf-media-sinks.md)puede obtener este conjunto de información del receptor de medios de ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) y [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) establecen el tipo de salida del codificador en el tipo de medio especificado por la aplicación.

**Nota**  Si usa [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) y [**MFCreateWMVEncoderActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) puede activar el codificador llamando a [**MFActivate::ActivateObject,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pero no puede cambiar los tipos de medios de entrada y salida del codificador ni puede cambiar ninguna de las propiedades de codificación.

Para obtener más información sobre cómo crear Media Foundation mediante objetos de activación, vea [Activation Objects](activation-objects.md).

**Para obtener el tipo de medio de destino del receptor de medios de ASF**

1.  Obtenga un puntero al puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del receptor de medios de ASF llamando a **IMFMediaSink::QueryInterface** en el receptor de medios de ASF y pasando **IID \_ IMFASFContentInfo** como identificador de interfaz.
2.  Obtiene el objeto de perfil de ASF asociado al objeto ContentInfo.
3.  Enumera las secuencias del perfil para obtener el tipo de medio de la secuencia.

**Para obtener las propiedades de codificación del receptor de medios de ASF**

1.  Si ha configurado [](configuring-the-encoder.md) las propiedades de codificación en el receptor multimedia (que se describe en Establecer propiedades en el receptor de [archivos),](setting-properties-in-the-file-sink.md)puede hacer referencia al almacén de propiedades del receptor llamando a **IMFMediaSink::QueryInterface** en el receptor de medios de ASF y pasando **\_ IID IPropertyStore** como identificador de interfaz.
2.  Si tiene un puntero al objeto ContentInfo del receptor, puede llamar a [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obtener una referencia al almacén de propiedades del receptor multimedia.

    Asegúrese de que todas las propiedades de codificación establecidas en el receptor de medios de ASF se reflejan en el almacén de propiedades pasado a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) y [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). El codificador se configura automáticamente en función de la configuración especificada por la aplicación.

Al crear el nodo de transformación en la topología de codificación, puede establecer el tipo de objeto como un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recibido en estas dos llamadas. Cuando se resuelve la topología, la sesión multimedia usa el objeto de activación para crear una instancia del MFT del codificador.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Enumeración de codificador en Windows 7 y versiones posteriores

En el caso de las aplicaciones que se ejecutan en Windows 7, además de [**MFTEnum,**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) puede enumerar las MFTEnum del codificador llamando a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Esta función devuelve un puntero al objeto de activación del MFT del codificador. La estructura de la función es muy similar a **MFTEnum** descrita anteriormente, salvo que **MFTEnumEx** devuelve una matriz de punteros [**DE TIPO MFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para los MFTEnum del codificador que coinciden con los criterios de búsqueda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> </dl>

 

 



