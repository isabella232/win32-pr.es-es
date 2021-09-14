---
title: Integración de información de álbum
description: Integración de información de álbum
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Reproductor de Windows Media en línea, integración de información de álbum
- online stores,album info integration
- tipo 2 tiendas en línea, integración de información de álbum
- Reproductor de Windows Media en línea, integración de la información del álbum
- tiendas en línea, integración de la información del álbum
- tiendas en línea de tipo 2, integración de la información del álbum
- Reproductor de Windows Media, integración de la información del álbum
- Reproductor de Windows Media,integración de información de álbum
- integración de información de álbum
- integración de la información del álbum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890145"
---
# <a name="album-info-integration"></a>Integración de información de álbum

Reproductor de Windows Media permite a los usuarios solicitar información detallada sobre el CD o DVD desde el que se originó el contenido multimedia digital haciendo clic en un botón, como **Más información.** Cuando el usuario hace clic en el botón, Reproductor de Windows Media 10 o posterior llama a en la tienda de música actual para mostrar los detalles del álbum. Cuando esto sucede, el reproductor abre el panel de información del álbum y muestra la página web especificada por el atributo **URL** del **elemento AlbumInfo** del documento ServiceInfo.

Reproductor de Windows Media una cadena de consulta a la dirección URL para proporcionar información a la tienda en línea sobre el contenido solicitado por el usuario. La cadena de consulta incluye atributos **como Title**, **Album** y **Artist,** que la tienda en línea puede usar para determinar el álbum correcto que se va a mostrar. La documentación de referencia del **elemento AlbumInfo** proporciona la lista completa de atributos de cadena de consulta y sus descripciones.

## <a name="guidelines-for-album-info"></a>Directrices para la información del álbum

Al crear la página web de información del álbum, use las siguientes directrices:

-   La página debe identificar claramente la tienda en línea que proporciona la información. Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.
-   La página debe incluir un vínculo a la declaración de privacidad de su empresa.
-   Evite la navegación por páginas dentro de la característica de información del álbum siempre que sea posible. Debe ir a la tienda en línea para la mayoría de las actividades.
-   Se recomienda proporcionar información valiosa sin necesidad de que el usuario instale programas o inicie sesión en su tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento AlbumInfo**](albuminfo-element.md)
</dt> </dl>

 

 




