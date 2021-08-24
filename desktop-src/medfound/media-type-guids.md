---
description: Tipos de medios principales
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Tipos de medios principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec660dcb86cfd1da5a80bef106ee8ddd17cf1e89899fea6b824fba5ab9be04e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715305"
---
# <a name="major-media-types"></a>Tipos de medios principales

En un tipo de medio, el *tipo principal* describe la categoría general de los datos, como audio o vídeo. El *subtipo*, si está presente, refina aún más el tipo principal. Por ejemplo, si el tipo principal es vídeo, el subtipo podría ser vídeo RGB de 32 bits. Los subtipos también distinguen los formatos codificados, como el vídeo H.264, de los formatos sin comprimir.

El tipo principal y el subtipo se identifican mediante GUID y se almacenan en los atributos siguientes:



| Atributo                                             | Descripción |
|-------------------------------------------------------|-------------|
| [TIPO \_ PRINCIPAL DE MT \_ DE \_ MF](mf-mt-major-type-attribute.md) | Tipo principal. |
| [\_SUBTIPO DE MT DE MF \_](mf-mt-subtype-attribute.md)        | Subtipo.    |



 

Se definen los siguientes tipos principales.



| Tipo principal                    | Descripción                                                                                                                                                | Subtipos                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **MFMediaType \_ Audio**        | Audio.                                                                                                                                                     | [GUID de subtipo de audio](audio-subtype-guids.md).      |
| **MFMediaType \_ Binary**       | Secuencia binaria.                                                                                                                                             | Ninguno.                                                |
| **MFMediaType \_ FileTransfer** | Secuencia que contiene archivos de datos.                                                                                                                         | Ninguno.                                                |
| **MFMediaType \_ HTML**         | Secuencia HTML.                                                                                                                                               | Ninguno.                                                |
| **Imagen \_ MFMediaType**        | Todavía secuencia de imágenes.                                                                                                                                        | [GUID de WIC y CLID](../wic/-wic-guids-clsids.md).       |
| **Metadatos de MFMediaType \_**        | Flujo de metadatos.                                                                                                                                        | Ninguno.       |
| **MFMediaType \_ Protected**    | Medios protegidos.                                                                                                                                           | El subtipo especifica el esquema de protección de contenido. |
| **MFMediaType \_ Perception**   | Secuencias desde un sensor de cámara o una unidad de procesamiento que razones y comprenden los datos de vídeo sin procesar y proporcionan comprensión del entorno o de los seres humanos que contiene. | Ninguno.                                                |
| **MFMediaType \_ SAMI**         | Subtítulos sincronizados de intercambio multimedia accesible (SAMI).                                                                                                 | Ninguno.                                                |
| **MFMediaType \_ Script**       | Secuencia de scripts.                                                                                                                                             | Ninguno.                                                |
| **MFMediaType \_ Stream**       | Flujo multiplexado o flujo elemental.                                                                                                                   | [GUID de subtipo de secuencia](stream-subtype-guids.md)     |
| **VÍDEO \_ MFMediaType**        | Video.                                                                                                                                                     | [GUID de subtipo de vídeo](video-subtype-guids.md).      |



 

Los componentes de terceros pueden definir nuevos tipos principales y nuevos subtipos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 
