---
description: Principales tipos de medios
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Principales tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003404"
---
# <a name="major-media-types"></a>Principales tipos de medios

En un tipo de medio, el *tipo principal* describe la categoría general de los datos, como audio o vídeo. El *subtipo*, si está presente, refina aún más el tipo principal. Por ejemplo, si el tipo principal es vídeo, el subtipo podría ser un vídeo RGB de 32 bits. Los subtipos también distinguen los formatos codificados, como el vídeo H. 264, de los formatos sin comprimir.

El tipo principal y el subtipo se identifican mediante GUID y se almacenan en los siguientes atributos:



| Atributo                                             | Descripción |
|-------------------------------------------------------|-------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md) | Tipo principal. |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)        | Subtipo.    |



 

Se definen los siguientes tipos principales.



| Tipo principal                    | Descripción                                                                                                                                                | Subtipos                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **\_Audio MFMediaType**        | Audio.                                                                                                                                                     | [GUID de subtipo de audio](audio-subtype-guids.md).      |
| **\_Binario MFMediaType**       | Secuencia binaria.                                                                                                                                             | Ninguno.                                                |
| **MFMediaType \_ FileTransfer** | Flujo que contiene archivos de datos.                                                                                                                         | Ninguno.                                                |
| **MFMediaType \_ HTML**         | Secuencia HTML.                                                                                                                                               | Ninguno.                                                |
| **Imagen de MFMediaType \_**        | Secuencia de imagen fija.                                                                                                                                        | [GUID y CLSID de WIC](../wic/-wic-guids-clsids.md).       |
| **MFMediaType \_ protegido**    | Medios protegidos.                                                                                                                                           | El subtipo especifica el esquema de protección de contenido. |
| **Percepción de MFMediaType \_**   | Secuencias de un sensor de cámara o una unidad de procesamiento que motiva y comprende datos de vídeo sin procesar y que proporciona información sobre el entorno o los seres humanos que contiene. | Ninguno.                                                |
| **MFMediaType \_ Sami**         | Subtítulos de intercambio de medios accesibles (SAMI) sincronizados.                                                                                                 | Ninguno.                                                |
| **\_Script MFMediaType**       | Secuencia de script.                                                                                                                                             | Ninguno.                                                |
| **\_Flujo MFMediaType**       | Secuencia multiplexada o secuencia elemental.                                                                                                                   | [GUID de subtipos de secuencia](stream-subtype-guids.md)     |
| **Vídeo de MFMediaType \_**        | Video.                                                                                                                                                     | [GUID de subtipo de vídeo](video-subtype-guids.md).      |



 

Los componentes de terceros pueden definir nuevos tipos principales y subtipos nuevos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 
