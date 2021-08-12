---
title: Elemento TextBox de VML
description: Elemento TextBox de VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b6ef160e975f00dd859e0f6db6f2821054a34815b3aef1ea19f520ad3d01a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597514"
---
# <a name="vml-textbox-element"></a>Elemento TextBox de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un cuadro de texto para una forma.

Los atributos siguientes modifican un cuadro de texto.



| Atributo                                                                    | Descripción                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Dirección](msdn-online-vml-direction-attribute.md)                         | Define la dirección del texto.                         |
| [Id](id-attribute--textbox--vml.md)                                         | Define un identificador único para el cuadro de texto.               |
| [Inserción](msdn-online-vml-inset-attribute.md)                                 | Especifica los valores de margen interno para el texto del cuadro de texto.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Define cómo una aplicación permitirá valores de conjunto personalizados. |
| [Diseño y Flow](msdn-online-vml-layout-flow-attribute.md)                     | Determina el flujo del texto en el cuadro de texto.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Define direcciones alternativas para el texto en los cuadros de texto.        |
| [MSO-Fit-Shape-to-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Determina si una forma se ajustará para ajustarse al texto.       |
| [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Determina si el texto se ajustará para ajustarse a una forma.       |
| [MSO-Layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Define el flujo de diseño alternativo para el texto en un cuadro de texto.   |
| [MSO-Next-Textbox](msdn-online-vml-mso-next-textbox-attribute.md)           | Especifica el siguiente cuadro de texto de una serie.                    |
| [Rotación de MSO](msdn-online-vml-mso-rotate-attribute.md)                       | Determina si el texto gira con una forma girada.      |
| [MSO-Text-Scale](msdn-online-vml-mso-text-scale-attribute.md)               | Define el factor de escalado para ajustar el texto a las formas.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Determina si el texto se puede seleccionar con un solo clic. |
| [V-Text-Anchor](msdn-online-vml-v-text-anchor-attribute.md)                 | Define el delimitador vertical del texto en un cuadro de texto.       |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

A continuación se muestra el código mínimo necesario para generar un cuadro de texto.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Tenga en cuenta que el texto que se muestra en el cuadro de texto está incluido en las etiquetas TextBox. El texto dentro de las etiquetas se puede modificar mediante etiquetas HTML normales.

**Ejemplo**

-   [Ejemplo simple de TextBox](/previous-versions/bb264075(v=vs.85))

 

 