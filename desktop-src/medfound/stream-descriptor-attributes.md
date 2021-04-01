---
description: Atributos de descriptor de secuencia
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Atributos de descriptor de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811533"
---
# <a name="stream-descriptor-attributes"></a>Atributos de descriptor de secuencia

## <a name="common-stream-descriptor-attributes"></a>Atributos de descriptor de secuencia comunes

Los siguientes atributos se aplican a los descriptores de flujo.



| Atributo                                                   | Descripción                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_idioma MF SD \_**](mf-sd-language-attribute.md)        | Especifica el idioma de una secuencia.                                                  |
| [MF \_ SD \_ mutuamente \_ excluyente](mf-sd-mutually-exclusive.md) | Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo. |
| [**MF \_ SD \_ protegido**](mf-sd-protected-attribute.md)      | Especifica si una secuencia contiene contenido protegido.                                |
| [\_nombre de \_ flujo \_ SD MF](mf-sd-stream-name.md)               | Contiene el nombre de una secuencia.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific atributos del descriptor de flujo

Los siguientes atributos se aplican a los descriptores de secuencia para los archivos de formato de sistema avanzado (ASF).



| Atributo                                                                                                                | Descripción                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Especifica el tamaño de búfer promedio necesario para una secuencia en un archivo ASF, en bytes.            |
| [**\_velocidad de \_ \_ \_ bits promedio de \_ datos \_ ASF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Especifica la velocidad de bits de datos media de una secuencia en un archivo ASF, en bits por segundo.        |
| [**\_Índice de \_ \_ \_ \_ ID. de idioma \_ de MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Especifica el idioma usado por una secuencia en un archivo ASF.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Especifica el tamaño de búfer máximo necesario para una secuencia en un archivo ASF, en bytes.            |
| [**\_velocidad de \_ \_ bits de \_ datos Max SD ASF EXTSTRMPROP máx \_ \_ .**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Especifica la velocidad de bits de datos máxima de una secuencia en un archivo ASF, en bits por segundo.         |
| [**\_plantilla de \_ \_ cumplimiento de dispositivos de metadatos ASF \_ \_ \_ de MF SD**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Especifica la plantilla de conformidad de dispositivos de una secuencia en un archivo ASF, en bits por segundo. |
| [**\_velocidad de \_ bits de ASF SD ASF \_ STREAMBITRATES \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Especifica la velocidad de bits media de una secuencia en un archivo ASF, en bits por segundo.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Atributos de descriptor de flujo de origen de medios SAMI

El atributo siguiente se aplica al descriptor de flujo para el origen de medios SAMI.



| Atributo                                                       | Descripción                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**\_ \_ idioma sami MF \_ SD**](mf-sd-sami-language-attribute.md) | Contiene el nombre del idioma de intercambio de medios accesibles (SAMI) sincronizado que se define para la secuencia. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



