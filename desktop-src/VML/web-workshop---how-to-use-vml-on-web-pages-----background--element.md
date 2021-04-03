---
title: Usar el elemento Background
description: Usar el elemento Background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web Workshop, elemento Background
- diseñar páginas web, elemento Background
- Lenguaje de marcado de vectores (VML), elemento Background
- VML (Lenguaje de marcado de vectores), elemento Background
- gráficos vectoriales, elemento Background
- Background (elemento)
- Elementos VML, Fondo
- Formas VML, elemento Background
- Lenguaje de marcado de vectores (VML), personalizar el fondo
- VML (Lenguaje de marcado de vectores), personalizar el fondo
- gráficos vectoriales, personalizar el fondo
- Formas VML, personalizar el fondo
- Personalización del fondo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904654"
---
# <a name="using-the-background-element"></a>Usar el elemento Background

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, veremos cómo puede personalizar el fondo de una página web mediante el `<background>` elemento proporcionado en VML.

Como ha aprendido en el tema [de `<fill>` uso](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , puede colocar el `<fill>` subelemento dentro de `<shape>` , `<shapetype>` o cualquier elemento de forma predefinido para describir cómo rellenar la forma.

Del mismo modo, puede colocar el `<fill>` subelemento dentro del `<background>` elemento para describir cómo rellenar el fondo de una página web. Después, puede usar los atributos de propiedad del `<fill>` subelemento para personalizar el efecto de relleno, como [relleno de degradado](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [relleno de patrón](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)o [relleno de imagen](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).

Por ejemplo, para dibujar un fondo con relleno degradado, puede escribir las líneas siguientes en la `<BODY>` región de la página web:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 