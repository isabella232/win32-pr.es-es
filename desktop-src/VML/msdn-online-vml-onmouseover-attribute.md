---
title: Atributo OnMouseOver VML
description: Atributo OnMouseOver VML
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8318235b660f92f3d82b2dd8dd15e2192e97a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078273"
---
# <a name="vml-onmouseover-attribute"></a>Atributo OnMouseOver VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Desencadena un evento de mouse para una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* onmouseover = " *expresión* " >

**Comentarios:**

Cuando el puntero del mouse está en la forma, se genera un evento "mouseover". El valor se genera mediante la palabra clave **this** (como referencia al objeto) seguida de la sintaxis del modelo de objetos. Por ejemplo, para cambiar el color de relleno a rojo, use lo siguiente:

onmouseover = "this. fillColor = ' red '"

Observe el uso de comillas simples y dobles para establecer la expresión.

*Atributo estándar de VML*

**Ejemplo**

Cuando el puntero del mouse está en la forma, el color de relleno pasará de rojo a verde.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Ejemplo del atributo OnMouseOver](/previous-versions/bb264088(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 