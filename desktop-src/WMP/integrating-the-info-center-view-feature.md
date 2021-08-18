---
title: Integración de la característica de vista del Centro de información
description: Integración de la característica de vista del Centro de información
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Reproductor de Windows Media en línea, integración de la vista del Centro de información
- tiendas en línea, integración de la vista del Centro de información
- tiendas en línea de tipo 1, integración de la vista del Centro de información
- tiendas en línea de tipo 2, integración de la vista del Centro de información
- Reproductor de Windows Media tiendas en línea,Vista del Centro de información
- tiendas en línea,Vista del Centro de información
- tipo 1 tiendas en línea,Vista del Centro de información
- tiendas en línea de tipo 2, vista del Centro de información
- integración de la vista del Centro de información
- Vista del Centro de información
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caea279f933c3cbb411da72aab9ddf971df5f38c69d7291ae4ac67f7b96ed91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135468"
---
# <a name="integrating-the-info-center-view-feature"></a>Integración de la característica de vista del Centro de información

Reproductor de Windows Media permite a los usuarios abrir y cerrar la característica Vista del Centro de información. La vista del Centro de información es la característica en la que los usuarios esperan encontrar información completa y extendida sobre contenido multimedia digital específico. Cuando el usuario elige abrir la vista del Centro de información, Reproductor de Windows Media llama a en el almacén de música actual para mostrar la página web de vista del Centro de información especificada por el atributo **URL** del elemento **InfoCenter** del documento ServiceInfo.

Para recuperar información sobre el contenido multimedia digital que se reproduce actualmente, debe insertar una instancia del control Reproductor de Windows Media en la página web y usar el modelo de objetos Player. Por ejemplo, para recuperar el título, puede usar el código JScript siguiente:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Directrices para la vista del Centro de información

Al crear la página **web de vista del Centro** de información, use las siguientes directrices:

-   La página debe identificar claramente el almacén en línea que proporciona la información. Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.
-   La página debe incluir un vínculo a la declaración de privacidad de la empresa.
-   Evite la navegación por páginas dentro de la característica Vista del Centro de información siempre que sea posible. Debe ir a la tienda en línea para la mayoría de las actividades.
-   Es mejor proporcionar información valiosa sin necesidad de que el usuario instale programas o inicie sesión en su tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Elemento InfoCenter**](infocenter-element.md)
</dt> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




