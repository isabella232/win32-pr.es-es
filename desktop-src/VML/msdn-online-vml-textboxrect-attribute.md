---
title: Atributo TextBoxRect de VML
description: Atributo TextBoxRect de VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077820"
---
# <a name="vml-textboxrect-attribute"></a>Atributo TextBoxRect de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define uno o varios cuadros de texto dentro de una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *Element* textboxrect = " *expresión* " >

**Sintaxis de script**

*Element* . textboxrect = "*expresión*"

*expresión* = de *elemento*. textboxrect

**Comentarios:**

Un cuadro de texto se define mediante uno o más conjuntos de números que especifican (en orden) los puntos izquierdo, superior, derecho e inferior del rectángulo. Varios conjuntos se delimitan mediante un punto y coma. El valor predeterminado es el mismo valor de dimensión que el rectángulo que lo contiene. Si se define más de un TextBox, los conjuntos cuádruples separados por comas que definen cada TextBox se separan mediante signos de punto y coma. Normalmente, los cuadros de texto aparecen en conjuntos de 1, 2, 3 o 6 rectángulos en una forma.

*Atributo estándar de VML*

**Ejemplo**

Se define un cuadro de texto de 95 unidades por 95 unidades y se colocan 5 unidades dentro de la esquina superior izquierda de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 