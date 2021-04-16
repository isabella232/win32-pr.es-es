---
title: Integración de la característica de vista de centro de información
description: Integración de la característica de vista de centro de información
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player tiendas en línea, integración de la vista del centro de información
- tiendas en línea, integración de la vista del centro de información
- Escriba 1 tiendas en línea, integrando la vista del centro de información
- Escriba 2 tiendas en línea, integrando la vista del centro de información
- Windows Media Player tiendas en línea, vista del centro de información
- tiendas en línea, vista del centro de información
- tipo 1 tiendas en línea, vista del centro de información
- tipo 2 tiendas en línea, vista del centro de información
- integración de la vista del centro de información
- Vista del centro de información
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685610"
---
# <a name="integrating-the-info-center-view-feature"></a>Integración de la característica de vista de centro de información

Windows Media Player permite a los usuarios abrir y cerrar la característica de vista de centro de información. Info Center View es la característica en la que los usuarios esperan encontrar información enriquecida y ampliada sobre contenido multimedia digital específico. Cuando el usuario elige abrir info Center View, Windows Media Player llama a en la tienda de música actual para mostrar la Página Web de la vista de info Center especificada por el atributo **URL** del elemento **Infocenter** del documento ServiceInfo.

Para recuperar información sobre el contenido multimedia digital que se está reproduciendo actualmente, debe incrustar una instancia del control de Windows Media Player en la página web y utilizar el modelo de objetos del reproductor. Por ejemplo, para recuperar el título, puede usar el siguiente código JScript:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Directrices para la vista del centro de información

Al crear la Página Web de la **vista de centro de información** , use las siguientes directrices:

-   La página debe identificar claramente la tienda en línea que proporciona la información. Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.
-   La página debe incluir un vínculo a la declaración de privacidad de la empresa.
-   Evite la navegación de página dentro de la característica de vista de centro de información siempre que sea posible. Debe navegar a la tienda en línea para la mayoría de las actividades.
-   Es mejor proporcionar información valiosa sin necesidad de que el usuario instale programas o inicie sesión en la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Elemento InfoCenter**](infocenter-element.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Usar el control Media Player de Windows en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




