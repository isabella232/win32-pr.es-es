---
title: Posición (atributo, forma) (VML)
description: Posición (atributo, forma) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421363"
---
# <a name="position-attribute-shapevml"></a>Posición (atributo, forma) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el tipo de posición utilizado para colocar un elemento. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Position: *Expression* " >

**Sintaxis de script**

*Element* . Style. position = "*expresión*"

*expresión* = de *Element*. Style. Position

**Comentarios:**

El atributo **Position** es similar al atributo **Position** HTML estándar que se usa con las hojas de estilos.

Estos valores incluyen:



| Value    | Descripción                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Predeterminada. El elemento se coloca según el flujo normal de la página. Se omiten los atributos **superior** e **izquierdo** . Si el objeto está delimitado en línea, que solo ocurre en Microsoft Word, se usa este valor. |
| absolute | El elemento se coloca en relación con el elemento primario, utilizando los atributos **superior** e **izquierdo** . Este valor lo usan los objetos flotantes de Microsoft Word y Microsoft Excel, y las diapositivas de Microsoft PowerPoint.                  |
| relative | El elemento se coloca según el flujo normal de la página, pero se utilizan los atributos **superior** e **izquierdo** . La superposición de los elementos superpuestos se rige por el atributo **Z-index** .                       |



 

*Atributo estándar de VML*

**Ejemplo**

La posición del rectángulo se muestra utilizando el estilo *relativo* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo de posición](/previous-versions/bb264090(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 