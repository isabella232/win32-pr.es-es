---
title: Usar el elemento Background
description: Usar el elemento Background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Taller web, elemento de fondo
- diseñar páginas web, elemento de fondo
- Lenguaje de marcado de vectores (VML),elemento background
- VML (Lenguaje de marcado de vectores),elemento background
- gráficos vectoriales, elemento de fondo
- elemento background
- Elementos de VML, fondo
- Formas de VML, elemento de fondo
- Lenguaje de marcado de vectores (VML), personalización de fondos
- VML (Lenguaje de marcado de vectores), personalización de fondos
- gráficos vectoriales, personalización de fondos
- Formas de VML, personalización de fondos
- personalización de fondos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb4a694aa5458a0eae01fcbf577f72da8b8f54b7efda506423565aee362ce2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512785"
---
# <a name="using-the-background-element"></a>Usar el elemento Background

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo puede personalizar el fondo de una página web mediante el `<background>` elemento proporcionado en VML.

Como ha aprendido en [ `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) el tema Usar, puede colocar el sub element dentro de , o cualquier elemento de forma predefinido para describir cómo rellenar `<fill>` la `<shape>` `<shapetype>` forma.

De forma similar, puede colocar el sub elemento dentro del elemento para describir cómo rellenar `<fill>` el fondo de una página `<background>` web. A continuación, puede usar los atributos de propiedad del sub elemento para personalizar el efecto de relleno, como relleno de `<fill>` [degradado,](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)relleno [de](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)patrón o relleno [de imagen.](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)

Por ejemplo, para dibujar un fondo relleno de degradado, puede escribir las siguientes líneas en la `<BODY>` región de la página web:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 