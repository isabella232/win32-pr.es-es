---
title: Compra de la integración para las tiendas en línea de tipo 2
description: Compra de la integración para las tiendas en línea de tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player tiendas en línea, integración de compras
- tiendas en línea, integración de compras
- tipo 2 tiendas en línea, integración de compras
- Windows Media Player tiendas en línea, integración de compras
- tiendas en línea, integración de compras
- tipo 2 tiendas en línea, integración de compras
- Windows Media Player, integración de compras
- Windows Media Player, integración de compras
- adquirir integración
- integración de compras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704719"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Compra de la integración para las tiendas en línea de tipo 2

Cuando Windows Media Player reproduce contenido multimedia digital o el usuario elige **Buscar información de álbum**, el reproductor ofrece al usuario un vínculo para comprar el CD o DVD desde el que se originó el contenido si dicho vínculo está disponible. Cuando el usuario hace clic en el vínculo, Windows Media Player 10 o una versión posterior llama a en la tienda de música actual para controlar la solicitud de compra. Cuando esto ocurre, el reproductor navega al primer panel de tareas de servicio (en Windows Media Player 10) o a la pestaña de tiendas en línea (en Windows Media Player 11) y muestra la Página Web especificada por el atributo **MediaPlayerURL** del elemento **BuyCD** del documento ServiceInfo. (Los atributos **MediaCenterURL** y **BrowserURL** se usan de forma similar para controlar las llamadas de Windows xp Media Center Edition 2004 y Windows XP Service Pack 2).

Windows Media Player anexa una cadena de consulta a la dirección URL para proporcionar información a la tienda en línea sobre el contenido que el usuario decidió comprar. La cadena de consulta incluye atributos como el **título**, el **álbum** y el **artista**, que la tienda en línea puede usar para determinar el álbum correcto que se va a vender. La documentación de referencia para el elemento **BuyCD** proporciona la lista completa de atributos de cadena de consulta y sus descripciones.

## <a name="guidelines-for-the-buycd-page"></a>Instrucciones para la página BuyCD

Al crear la Página Web de BuyCD, use las siguientes directrices:

-   La página debe identificar claramente la tienda en línea que proporciona la información. Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.
-   La página debe incluir un vínculo a la declaración de privacidad de la empresa.
-   Es mejor proporcionar información de compra inicial sin necesidad de que el usuario instale programas o inicie sesión en la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento BuyCD**](buycd-element.md)
</dt> </dl>

 

 




