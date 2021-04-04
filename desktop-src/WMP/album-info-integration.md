---
title: Integración de información de álbumes
description: Integración de información de álbumes
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player tiendas en línea, integración de información de álbumes
- tiendas en línea, integración de información de álbumes
- tipo 2 tiendas en línea, integración de información de álbumes
- Windows Media Player tiendas en línea, integración de información de álbumes
- tiendas en línea, integración de información de álbumes
- tipo 2 tiendas en línea, información de álbumes de integración
- Windows Media Player, integración de la información del álbum
- Windows Media Player, integración de información de álbumes
- integración de información de álbumes
- integración de la información del álbum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075641"
---
# <a name="album-info-integration"></a>Integración de información de álbumes

Windows Media Player permite a los usuarios solicitar información detallada sobre el CD o DVD desde el que se origina el contenido multimedia digital al hacer clic en un botón, como **más información**. Cuando el usuario hace clic en el botón, Windows Media Player 10 o una versión posterior llama a en la tienda de música actual para mostrar los detalles del álbum. Cuando esto ocurre, el reproductor abre el panel de información del álbum y muestra la Página Web especificada por el atributo **URL** del elemento **AlbumInfo** del documento ServiceInfo.

Windows Media Player anexa una cadena de consulta a la dirección URL para proporcionar información a la tienda en línea sobre el contenido solicitado por el usuario. La cadena de consulta incluye atributos como el **título**, el **álbum** y el **artista**, que la tienda en línea puede usar para determinar el álbum correcto que se va a mostrar. La documentación de referencia para el elemento **AlbumInfo** proporciona la lista completa de atributos de cadena de consulta y sus descripciones.

## <a name="guidelines-for-album-info"></a>Directrices para la información del álbum

Al crear la Página Web de información del álbum, siga estas instrucciones:

-   La página debe identificar claramente la tienda en línea que proporciona la información. Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.
-   La página debe incluir un vínculo a la declaración de privacidad de la empresa.
-   Evite la navegación por la página dentro de la característica información del álbum siempre que sea posible. Debe navegar a la tienda en línea para la mayoría de las actividades.
-   Le recomendamos que proporcione información valiosa sin necesidad de que el usuario instale programas o inicie sesión en la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento AlbumInfo**](albuminfo-element.md)
</dt> </dl>

 

 




