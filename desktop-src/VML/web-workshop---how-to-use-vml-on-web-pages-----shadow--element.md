---
title: Usar el elemento Shadow
description: Usar el elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web Workshop, elemento Shadow
- diseñar páginas web, elemento Shadow
- Lenguaje de marcado de vectores (VML), elemento Shadow
- VML (Lenguaje de marcado de vectores), elemento Shadow
- gráficos vectoriales, elemento Shadow
- elemento Shadow
- Elementos VML, sombra
- Formas VML, elemento Shadow
- Lenguaje de marcado de vectores (VML), dibujar con efectos de sombra
- VML (Lenguaje de marcado de vectores), dibujar con efectos de sombra
- gráficos vectoriales, dibujar con efectos de sombra
- Formas VML, dibujar con efectos de sombra
- dibujar con efectos de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421315"
---
# <a name="using-the-shadow-element"></a>Usar el elemento Shadow

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo usar el `<shadow>` subelemento para dibujar una forma que tiene varios efectos de sombra.

Puede colocar el `<shadow>` subelemento dentro de `<shape>` , `<shapetype>` o cualquier elemento de forma predefinido para dibujar una forma con una sombra. Después, puede usar los atributos de propiedad del `<shadow>` subelemento para personalizar la sombra.

Por ejemplo, para crear una forma con una sombra, tal como se muestra en la siguiente imagen, puede escribir las líneas siguientes en la `<BODY>` región de la página web:

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` e `type="perspective"` indican que debe activar la sombra con el tipo de perspectiva.
-   El **origen** y el **desplazamiento** indican dónde dibujar la sombra.
-   `matrix="..."` Especifica la matriz de transformación de perspectiva.

Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 