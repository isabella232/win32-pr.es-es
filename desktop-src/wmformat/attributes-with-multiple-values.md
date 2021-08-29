---
title: Atributos con varios valores (Windows SDK de formato multimedia 11)
description: Obtenga información sobre los atributos con varios valores en el SDK Windows Media Format 11. Algunos atributos de elementos multimedia pueden tener varios valores.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows SDK de formato multimedia, atributos
- Formato de sistemas avanzados (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- attributes,multiple values
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e87ff070b4714d7d9bc7eb5fcc7728bc4c39bc964a14d8545eff2023967a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709495"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Atributos con varios valores (Windows SDK de formato multimedia 11)

Algunos de los atributos predefinidos pueden tener varios valores asignados. Por ejemplo, **Artist** es un atributo que puede tener varios valores. Puede llamar a [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) varias veces para agregar tantos valores **de Artist** como necesite. Si realiza varias llamadas a **AddAttribute** para atributos que no admiten varios valores, el método puede devolver un código de error o simplemente omitir la solicitud.

En la tabla siguiente se enumeran los atributos que admiten varios valores. Algunos atributos solo pueden tener varios valores en archivos ASF, mientras que otros pueden tener varios valores en archivos ASF y MP3.



| Atributo                                                 | Compatibilidad con varios valores |
|-----------------------------------------------------------|-----------------------------|
| [**Autor**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | asf                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | asf                         |
| [**WM/Category**](wm-category.md)                        | asf                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/Conductor**](wm-conductor.md)                      | asf                         |
| [**WM/Director**](wm-director.md)                        | asf                         |
| [**WM/Genre**](wm-genre.md)                              | asf                         |
| [**WM/GenreID**](wm-genreid.md)                          | asf                         |
| [**WM/Language**](wm-language.md)                        | ASF, MP3                    |
| [**\_WM/Sincronización de wm/desastroso**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/Estados de ánimo**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/Picture**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | asf                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | asf                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




