---
title: Atributo alternativo VML
description: Atributo alternativo VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271353"
---
# <a name="vml-alt-attribute"></a>Atributo alternativo VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el texto alternativo que se va a mostrar en lugar de un gráfico. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* Alt = " *expresión* " >

**Sintaxis de script**

*Element* . Alt = "*expresión*"

*expresión* = de *elemento*. Alt

**Comentarios:**

El atributo **Alt** es similar al atributo **Alt** de HTML estándar. Este atributo proporciona una manera para que los exploradores que convierten texto en voz describan los elementos gráficos de una página.

*Atributo estándar de VML*

**Vea también**

[Forma](shape-element--vml.md)

**Ejemplo**

En el elemento **Alt** siguiente se mostrará la frase "rectángulo rojo" en los exploradores que convierten las páginas web en frases habladas.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo del atributo ALT](/previous-versions/bb229663(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 