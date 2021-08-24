---
title: Usar el elemento Shadow
description: Usar el elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Taller web, elemento shadow
- diseñar páginas web, elemento shadow
- Lenguaje de marcado de vectores (VML),elemento shadow
- VML (Lenguaje de marcado de vectores),shadow element
- gráficos vectoriales, elemento shadow
- shadow, elemento
- Elementos vml, sombra
- Formas de VML, elemento de sombra
- Lenguaje de marcado de vectores (VML),dibujar con efectos de sombra
- VML (Lenguaje de marcado de vectores),dibujar con efectos de sombra
- gráficos vectoriales, dibujo con efectos de sombra
- Formas de VML, dibujo con efectos de sombra
- dibujo con efectos de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83be3f59eacfb495a2c80d212bc99cfd3d43be10aa8144eb68d3defd8a029e41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512605"
---
# <a name="using-the-shadow-element"></a>Usar el elemento Shadow

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo usar el sub elemento para `<shadow>` dibujar una forma que tiene varios efectos de sombra.

Puede colocar el sub elemento dentro de , o cualquier elemento de forma predefinido `<shadow>` para dibujar una forma con una `<shape>` `<shapetype>` sombra. A continuación, puede usar los atributos de propiedad del `<shadow>` sub elemento para personalizar la sombra.

Por ejemplo, para crear una forma con una sombra, como se muestra en la siguiente imagen, puede escribir las siguientes líneas en la `<BODY>` región de la página web:

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` e `type="perspective"` indican para activar la sombra mediante el tipo de perspectiva.
-   El **origen y** el **desplazamiento** indican dónde dibujar la sombra.
-   `matrix="..."` especifica la matriz de transformación de perspectiva.

Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 