---
description: Para convertir archivos multimedia en formato ASF, puede usar codificadores de Windows Media. Para usar estos codificadores, se deben registrar con el sistema.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Usar objetos de activación de codificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd44a1b97ad0f133b7215ff4474835ddfba66bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908633"
---
# <a name="using-an-encoders-activation-objects"></a>Usar objetos de activación del codificador

Para convertir archivos multimedia en formato ASF, puede usar codificadores de Windows Media. Para usar estos codificadores, se deben registrar con el sistema.

Para obtener información sobre el registro del codificador, consulte [crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md).

-   [Usar objetos de activación del codificador](#using-an-encoders-activation-objects)
-   [Enumeración del codificador en Windows 7 y versiones posteriores](#encoder-enumeration-in-windows-7-and-later)
-   [Temas relacionados](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Usar objetos de activación del codificador

Como alternativa al uso de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de un codificador (descrita en [creación de un codificador mediante CoCreateInstance](using-an-encoder-s-imftransform--interface.md)), puede crear una instancia del objeto de activación para el codificador. Los objetos de activación facilitan la creación y el Media Foundation del codificador proporcionan las dos funciones siguientes para este enfoque:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) para crear una instancia del codificador de audio de Windows Media.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) para crear una instancia del codificador de vídeo de Windows Media.

Ambas funciones requieren que se cree el tipo de medio de destino y se establezcan las propiedades de codificación antes de llamar a estas funciones. Si la aplicación usa [componentes ASF de capa de canalización](pipeline-layer-asf-components.md) para codificar un archivo en formato ASF y ya ha creado y configurado los [receptores de medios ASF](asf-media-sinks.md), puede obtener este conjunto de información del receptor de medios ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) y [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) establecen el tipo de salida del codificador en el tipo de medio especificado por la aplicación.

**Nota:**  Si usa [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) y [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) , puede activar el codificador llamando a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , pero no puede cambiar la entrada y los tipos de medios de salida del codificador ni puede cambiar ninguna de las propiedades de codificación.

Para obtener más información sobre cómo crear objetos Media Foundation mediante el uso de objetos de activación, vea [objetos de activación](activation-objects.md).

**Para obtener el tipo de medio de destino del receptor de medios ASF**

1.  Obtiene un puntero al puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del receptor multimedia ASF llamando a **IMFMediaSink:: QueryInterface** en el receptor de medios ASF y pasando el **IID \_ IMFASFContentInfo** como identificador de interfaz.
2.  Obtiene el objeto de perfil ASF asociado al objeto ContentInfo.
3.  Enumerar las secuencias del perfil para obtener el tipo de archivo multimedia de la secuencia.

**Para obtener las propiedades de codificación del receptor multimedia ASF**

1.  Si ha configurado las [propiedades de codificación](configuring-the-encoder.md) en el receptor de medios (que se describe en [configuración de las propiedades del receptor de archivos](setting-properties-in-the-file-sink.md)), puede hacer referencia al almacén de propiedades del receptor mediante una llamada a **IMFMediaSink:: QueryInterface** en el receptor de medios ASF y pasar el **IID \_ IPropertyStore** como identificador de interfaz.
2.  Si tiene un puntero al objeto ContentInfo del receptor, puede llamar a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obtener una referencia al almacén de propiedades del receptor de medios.

    Asegúrese de que todas las propiedades de codificación que se establecen en el receptor de medios ASF se reflejan en el almacén de propiedades que se pasa a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) y [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). El codificador se configura automáticamente en función de la configuración especificada por la aplicación.

Al crear el nodo de transformación en la topología de codificación, puede establecer el tipo de objeto como un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recibido en estas dos llamadas. Cuando se resuelve la topología, la sesión multimedia utiliza el objeto de activación para crear una instancia de la MFT del codificador.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Enumeración del codificador en Windows 7 y versiones posteriores

En el caso de las aplicaciones que se ejecutan en Windows 7, además de [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) puede enumerar el codificador MFTs mediante una llamada a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Esta función devuelve un puntero al objeto de activación de la MFT del codificador. La estructura de la función es muy similar a **MFTEnum** descrita anteriormente, salvo que **MFTEnumEx** devuelve una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para el codificador MFTs que coinciden con los criterios de búsqueda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> </dl>

 

 



