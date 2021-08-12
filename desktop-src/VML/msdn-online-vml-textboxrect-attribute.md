---
title: Atributo TextBoxRect de VML
description: Atributo TextBoxRect de VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644d4a89effa54a991d04de4c97c4f9d86876a78d86149d9b99c3a8161585b44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597487"
---
# <a name="vml-textboxrect-attribute"></a>Atributo TextBoxRect de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uno o varios cuadros de texto dentro de una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* textboxrect=" *expression* ">

**Sintaxis de script**

*element* .textboxrect="*expression*"

*expresión* = *elemento*.textboxrect

**Comentarios:**

Un cuadro de texto se define mediante uno o varios conjuntos de números que especifican (en orden) los puntos izquierdo, superior, derecho e inferior del rectángulo. Varios conjuntos se delimitan mediante un punto y coma. El valor predeterminado es el mismo valor de dimensión que el rectángulo que lo contiene. Si se define más de un cuadro de texto, los conjuntos delimitados por comas que definen cada cuadro de texto se separan por punto y coma. Normalmente, los cuadros de texto se incluyen en conjuntos de 1, 2, 3 o 6 rectángulos en una forma.

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



 

 