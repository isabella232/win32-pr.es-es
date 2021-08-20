---
title: Usar elementos PARAM en una página web mostrada por Firefox
description: Usar elementos PARAM en una página web mostrada por Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Reproductor de Windows Media,PARAM en el elemento OBJECT
- Reproductor de Windows Media modelo de objetos, elementos PARAM en el elemento OBJECT
- object model,PARAM elements in OBJECT element
- Reproductor de Windows Media Elementos Mobile,PARAM en el elemento OBJECT
- Reproductor de Windows Media ActiveX control, elementos PARAM en el elemento OBJECT
- Reproductor de Windows Media Control ActiveX móvil, elementos PARAM en el elemento OBJECT
- ActiveX control, elementos PARAM en el elemento OBJECT
- embedding,Web pages
- Incrustación de páginas web, elementos PARAM en el elemento OBJECT
- Elementos PARAM del elemento OBJECT
- Reproductor de Windows Media,Firefox
- Reproductor de Windows Media modelo de objetos,Firefox
- object model,Firefox
- Reproductor de Windows Media Mobile,Firefox
- Reproductor de Windows Media ActiveX control,Firefox
- Reproductor de Windows Media Control de ActiveX móvil,Firefox
- ActiveX control, Firefox
- Elementos Firefox,PARAM en el elemento OBJECT
- Inserción de páginas web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767b9b0d5e4367a17f07f68600ff8e9cac488ca9e4c950165d84677fd7d03956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117310"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Usar elementos PARAM en una página web mostrada por Firefox

Puede usar elementos PARAM dentro de un elemento OBJECT para establecer el estado inicial del control Player. Por ejemplo, los elementos PARAM del ejemplo siguiente especifican que el control debe reproducir seattle.wmv automáticamente.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



La mayoría de los elementos PARAM se pueden interpretar Internet Explorer y Firefox. Sin embargo, hay algunos elementos PARAM que el complemento firefox no admite. Para obtener información sobre qué elementos PARAM son compatibles con el complemento firefox, vea [Elementos PARAM en un elemento OBJECT](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de Reproductor de Windows Media Control con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




