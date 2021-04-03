---
title: Elemento TextBox de VML
description: Elemento TextBox de VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791824"
---
# <a name="vml-textbox-element"></a>Elemento TextBox de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un cuadro de texto para una forma.

Los atributos siguientes modifican un cuadro de texto.



| Atributo                                                                    | Descripción                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Dirección](msdn-online-vml-direction-attribute.md)                         | Define la dirección del texto.                         |
| [Id](id-attribute--textbox--vml.md)                                         | Define un identificador único para el cuadro de texto.               |
| [Hundi](msdn-online-vml-inset-attribute.md)                                 | Especifica los valores de margen interno del texto del cuadro de texto.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Define el modo en que una aplicación permitirá valores de bajorrelieve personalizados. |
| [Flujo de diseño](msdn-online-vml-layout-flow-attribute.md)                     | Determina el flujo del texto en el cuadro de texto.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Define direcciones alternativas para el texto en los cuadros de texto.        |
| [MSO-ajustar: forma a texto](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Determina si una forma se ajustará para ajustarse al texto.       |
| [MSO-ajustar: texto a forma](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Determina si el texto se ajustará para ajustarse a una forma.       |
| [MSO-layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Define el flujo de diseño alternativo para el texto en un cuadro de texto.   |
| [MSO-Next-TextBox](msdn-online-vml-mso-next-textbox-attribute.md)           | Especifica el siguiente cuadro de texto de una serie.                    |
| [MSO-girar](msdn-online-vml-mso-rotate-attribute.md)                       | Determina si el texto gira con una forma girada.      |
| [MSO-escala de texto](msdn-online-vml-mso-text-scale-attribute.md)               | Define el factor de escala para ajustar el texto a las formas.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Determina si el texto es seleccionable con un solo clic. |
| [V-Text-Anchor](msdn-online-vml-v-text-anchor-attribute.md)                 | Define la delimitación vertical del texto en un cuadro de texto.       |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

A continuación se encuentra el código mínimo necesario para generar un cuadro de texto.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Tenga en cuenta que el texto que se muestra en el cuadro de texto está incluido en las etiquetas del cuadro de texto. El texto dentro de las etiquetas puede ser modificado por etiquetas HTML normales.

**Ejemplo**

-   [Ejemplo de cuadro de texto simple](/previous-versions/bb264075(v=vs.85))

 

 