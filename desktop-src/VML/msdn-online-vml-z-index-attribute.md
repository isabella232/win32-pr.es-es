---
title: Atributo Z-index de VML
description: Atributo Z-index de VML
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995320"
---
# <a name="vml-z-index-attribute"></a>Atributo Z-index de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina el orden de presentación de las formas superpuestas. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "z-index: *Expression* " >

**Sintaxis de script**

*Element* . Style. ZIndex = "*expresión*"

*expresión* = de *elemento*. Style. ZIndex

**Comentarios:**

El atributo **z-index** es similar al atributo **z-index** de HTML estándar para los estilos.

Estos valores incluyen:



| Value | Descripción                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático  | Se utilizará el orden en que se muestran las formas en la página HTML, de abajo a arriba.                                                                                                                         |
| orden | Número que representa la precedencia de la pila. Una forma con un número mayor se mostrará como si wereoverlapping (en "Front") una forma con un número inferior. Se pueden usar números negativos. |



 

*Atributo estándar de VML*

**Ejemplo**

La forma roja se mostrará en "Front" de la forma azul, porque tiene un índice z superior.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Ejemplo de atributo de índice Z](/previous-versions/ms530275(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 