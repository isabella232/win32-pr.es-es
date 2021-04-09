---
title: Atributo de bajorrelieve (VML)
description: Atributo de bajorrelieve (VML)
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149351"
---
# <a name="vml-inset-attribute"></a>Atributo de bajorrelieve (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica los valores de margen interno del texto del cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *elemento* bajorrelieve = " *expresión* " >

**Sintaxis de script**

*Element* . bajorrelieve = "*expresión*"

*expresión* = de *elemento*. bajorrelieve

**Comentarios:**

El valor del margen de texto interno se especifica como una cadena que contiene cuatro valores, separados por comas o espacios. Los valores se miden desde los bordes izquierdo, superior, derecho e inferior del cuadro especificado por el atributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) de **path**. Los valores que faltan se establecen en el valor predeterminado, que es "0.1 en, 0,05 en, 0.1 en, 0,05 en".

En el caso de las formas giradas en los exploradores que no admiten la rotación, el cuadro de límite se ajustará al múltiplo más cercano de 90 grados.

*Atributo estándar de VML*

**Ejemplo**

El cuadro de texto tendrá un margen de bajorrelieve de 10 píxeles.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 