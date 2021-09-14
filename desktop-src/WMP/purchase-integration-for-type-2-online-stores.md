---
title: Integración de compras para tiendas en línea de tipo 2
description: Integración de compras para tiendas en línea de tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Reproductor de Windows Media en línea, integración de compras
- tiendas en línea, integración de compras
- tipo 2 tiendas en línea, integración de compras
- Reproductor de Windows Media en línea, integración de compras
- tiendas en línea, integración de compras
- tiendas en línea de tipo 2, integración de compras
- Reproductor de Windows Media, integración de compras
- Reproductor de Windows Media, integración de compras
- integración de compra
- integración de compras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070957"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Integración de compras para tiendas en línea de tipo 2

Cuando Reproductor de Windows Media contenido multimedia digital o el usuario elige Buscar información del **álbum,** el reproductor ofrece al usuario un vínculo para comprar el CD o DVD desde el que se originó el contenido si este vínculo está disponible. Cuando el usuario hace clic en el vínculo, Reproductor de Windows Media 10 o posterior llama a en la tienda de música actual para controlar la solicitud de compra. Cuando esto sucede, el Reproductor navega al primer panel de tareas de servicio (en Reproductor de Windows Media 10) o a la pestaña Tiendas en línea (en Reproductor de Windows Media 11) y muestra la página web especificada por el atributo **MediaPlayerURL** del **elemento BuyCD** del documento ServiceInfo. (Los **atributos MediaCenterURL** y **BrowserURL** se usan de forma similar para controlar las llamadas desde Windows XP Media Center Edition 2004 y Windows XP Service Pack 2).

Reproductor de Windows Media una cadena de consulta a la dirección URL para proporcionar información a la tienda en línea sobre el contenido que el usuario eligió comprar. La cadena de consulta incluye atributos **como Title**, **Album** y **Artist,** que la tienda en línea puede usar para determinar el álbum correcto que se va a vender. La documentación de referencia del **elemento BuyCD** proporciona la lista completa de atributos de cadena de consulta y sus descripciones.

## <a name="guidelines-for-the-buycd-page"></a>Directrices para la página BuyCD

Al crear la página web de BuyCD, use las siguientes directrices:

-   La página debe identificar claramente la tienda en línea que proporciona la información. Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.
-   La página debe incluir un vínculo a la declaración de privacidad de su empresa.
-   Es mejor proporcionar información de compra inicial sin necesidad de que el usuario instale programas o inicie sesión en su tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento BuyCD**](buycd-element.md)
</dt> </dl>

 

 




