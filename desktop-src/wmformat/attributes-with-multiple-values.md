---
title: Atributos con varios valores (Windows Media Format 11 SDK)
description: Atributos con varios valores
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, varios valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078716"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Atributos con varios valores (Windows Media Format 11 SDK)

Algunos de los atributos predefinidos pueden tener varios valores asignados. Por ejemplo, **artista** es un atributo que puede tener varios valores. Puede llamar a [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) varias veces para agregar tantos valores de **intérprete** como necesite. Si realiza varias llamadas a **AddAttribute** para los atributos que no admiten varios valores, el método puede devolver un código de error o simplemente omitir la solicitud.

En la tabla siguiente se enumeran los atributos que admiten varios valores. Algunos atributos solo pueden tener varios valores en archivos ASF, mientras que otros pueden tener varios valores en archivos ASF y MP3.



| Atributo                                                 | Compatibilidad con varios valores |
|-----------------------------------------------------------|-----------------------------|
| [**Autor**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | asf                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | asf                         |
| [**WM/categoría**](wm-category.md)                        | asf                         |
| [**WM/compositor**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/conductor**](wm-conductor.md)                      | asf                         |
| [**WM/Director**](wm-director.md)                        | asf                         |
| [**WM/género**](wm-genre.md)                              | asf                         |
| [**WM/GenreID**](wm-genreid.md)                          | asf                         |
| [**WM/lenguaje**](wm-language.md)                        | ASF, MP3                    |
| [**WM/Letras \_ sincronizadas**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/humor**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/imagen**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/productor**](wm-producer.md)                        | asf                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | asf                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/escritor**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




