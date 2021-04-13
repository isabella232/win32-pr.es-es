---
title: Atributo de modo encapsulado de VML MSO
description: Atributo de modo encapsulado de VML MSO
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359128"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Atributo de modo encapsulado de VML MSO

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el modo de ajuste del texto. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "MSO-Wrap-Mode: *expresión* " >

**Comentarios:**

Estos valores incluyen:



| Value          | Descripción                          |
|----------------|--------------------------------------|
| square         | Ajusta el texto alrededor de la forma de un cuadrado. |
| acoplamiento          | El texto se ajusta cerca de la forma.  |
| superior e inferior | El texto salta de arriba abajo.       |
| a través de        | El texto se muestra a través de la forma.     |
| ninguno           | El texto no se ajusta.                   |



 

Microsoft PowerPoint lo usa para guardar en HTML para indicar si el ajuste de palabra dentro de una autoforma está activado (**cuadrado**) o desactivado (**ninguno**).

*Microsoft Office atributo Extensions*

**Ejemplo**

El código siguiente indica que WordWrap está activado en PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 