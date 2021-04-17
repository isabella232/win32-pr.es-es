---
title: Usar elementos PARAM en una página web que se muestra en Firefox
description: Usar elementos PARAM en una página web que se muestra en Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player, elementos PARAM en el elemento OBJECT
- Modelo de objetos de Windows Media Player, elementos PARAM en el elemento OBJECT
- modelo de objetos, elementos PARAM en el elemento OBJECT
- Windows Media Player Mobile, elementos PARAM en el elemento OBJECT
- Control ActiveX de Windows Media Player, elementos PARAM en el elemento OBJECT
- Control ActiveX móvil de Windows Media Player, elementos PARAM en el elemento OBJECT
- Control ActiveX, elementos PARAM en el elemento OBJECT
- incrustación, páginas web
- Incrustación de páginas web, elementos PARAM en el elemento OBJECT
- Elementos PARAM en el elemento OBJECT
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Windows Media Player Mobile, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX móvil de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, elementos PARAM en el elemento OBJECT
- Incrustación de páginas web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104357820"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Usar elementos PARAM en una página web que se muestra en Firefox

Puede usar elementos PARAM dentro de un elemento OBJECT para establecer el estado inicial del control Player. Por ejemplo, los elementos PARAM en el ejemplo siguiente especifican que el control debería reproducir Seattle. wmv automáticamente.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



La mayoría de los elementos PARAM se pueden interpretar por Internet Explorer y Firefox. Sin embargo, hay algunos elementos PARAM que no admite el complemento Firefox. Para obtener información sobre los elementos de parámetro admitidos por el complemento de Firefox, vea [elementos param en un elemento Object](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del control de Media Player de Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




