---
title: Acerca de los metadatos
description: Acerca de los metadatos
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Media Player de Windows, metadatos
- metadatos, acerca de
- metadatos, atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356733"
---
# <a name="about-the-metadata"></a>Acerca de los metadatos

Windows Media Player 10 o posterior intenta sincronizar los siguientes atributos de metadatos.



| Atributo Player | Constante global de WMDM  | Descripción                                                                                                 | Versión requerida                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | **Cadena** terminada en null que contiene el nombre del intérprete principal del álbum.                         | Windows Media Player 11 o posterior. |
| Álbum            | g \_ wszWMDMAlbumTitle  | **Cadena** terminada en null que contiene el título del álbum en el que se liberó originalmente el contenido.  | Windows Media Player 11 o posterior. |
| Autor           | g \_ wszWMDMAuthor      | **Cadena** terminada en null que contiene el nombre del intérprete multimedia o actor asociado con el contenido.    | Windows Media Player 11 o posterior. |
| BuyNow           | g \_ wszWMDMBuyNow      | **Valor booleano** que indica si el usuario ha elegido comprar el contenido.                                 | Windows Media Player 10 o posterior. |
| WM/género         | g \_ wszWMDMGenre       | **Cadena** terminada en null que contiene el género del contenido.                                             | Windows Media Player 11 o posterior. |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD** que contiene el número de veces que el usuario ha reproducido el archivo multimedia digital.                        | Windows Media Player 10 o posterior. |
| ReleaseDate      | g \_ wszWMDMYear        | Fecha de la versión original del elemento.                                                               | Windows Media Player 11 o posterior. |
| Title            | g \_ wszWMDMTitle       | **Cadena** terminada en null que contiene el título.                                                            | Windows Media Player 11 o posterior. |
| WM/TrackNumber   | g \_ wszWMDMTrack       | **DWORD** que contiene el número de pista del elemento en el álbum en el que se liberó originalmente.         | Windows Media Player 11 o posterior. |
| UserRating       | g \_ wszWMDMUserRating  | **DWORD** que contiene un valor que representa la clasificación por estrellas del usuario especificado para el archivo multimedia digital. | Windows Media Player 10 o posterior. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia de metadatos acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




