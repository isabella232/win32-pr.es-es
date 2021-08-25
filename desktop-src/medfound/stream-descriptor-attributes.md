---
description: Atributos de descriptor de flujo
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Atributos de descriptor de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db29ef0076415ff07e9ed25f7e6ca3e0588ec25257802fe0c7829ab3178c935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953235"
---
# <a name="stream-descriptor-attributes"></a>Atributos de descriptor de flujo

## <a name="common-stream-descriptor-attributes"></a>Atributos comunes del descriptor de flujo

Los atributos siguientes se aplican a los descriptores de flujo.



| Atributo                                                   | Descripción                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**IDIOMA \_ MF SD \_**](mf-sd-language-attribute.md)        | Especifica el idioma de una secuencia.                                                  |
| [MF \_ SD \_ \_ MUTUAMENTE EXCLUYENTE](mf-sd-mutually-exclusive.md) | Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo. |
| [**MF \_ SD \_ PROTECTED**](mf-sd-protected-attribute.md)      | Especifica si una secuencia contiene contenido protegido.                                |
| [NOMBRE \_ DE FLUJO MF SD \_ \_](mf-sd-stream-name.md)               | Contiene el nombre de una secuencia.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific descriptores de flujo

Los atributos siguientes se aplican a los descriptores de secuencia para los archivos de formato de sistemas avanzados (ASF).



| Atributo                                                                                                                | Descripción                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Especifica el tamaño medio de búfer necesario para una secuencia en un archivo ASF, en bytes.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Especifica la velocidad media de bits de datos de una secuencia en un archivo ASF, en bits por segundo.        |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE \_ ID \_ INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Especifica el idioma utilizado por una secuencia en un archivo ASF.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Especifica el tamaño máximo de búfer necesario para una secuencia en un archivo ASF, en bytes.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Especifica la velocidad máxima de bits de datos de una secuencia en un archivo ASF, en bits por segundo.         |
| [**PLANTILLA \_ DE CONFORMIDAD DE \_ DISPOSITIVOS DE \_ \_ METADATOS \_ DE ASF MF SD \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Especifica la plantilla de conformidad del dispositivo para una secuencia en un archivo ASF, en bits por segundo. |
| [**VELOCIDAD \_ DE BITS DE \_ \_ STREAMBITRATES DE ASF \_ MF SD**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Especifica la velocidad de bits media de una secuencia en un archivo ASF, en bits por segundo.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Atributos del descriptor de flujo de origen de medios SAMI

El atributo siguiente se aplica al descriptor de secuencia para el origen multimedia SAMI.



| Atributo                                                       | Descripción                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ SAMI \_ LANGUAGE**](mf-sd-sami-language-attribute.md) | Contiene el nombre de lenguaje SAMI (Intercambio multimedia accesible sincronizado) que se define para la secuencia. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



