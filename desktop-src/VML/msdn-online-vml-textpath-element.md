---
title: Elemento TextPath de VML
description: Elemento TextPath de VML
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df22c7c9b26a4bdc40bb7ec82ee1d46af81018251f40a91302f3d97b4a7f174
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939303"
---
# <a name="vml-textpath-element"></a>Elemento TextPath de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un trazado de texto para una forma.

Los atributos siguientes modifican una ruta de acceso de texto.



| Atributo                                                                    | Descripción                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FitPath](msdn-online-vml-fitpath-attribute.md)                             | Define si el texto se ajusta al trazado de una forma.                             |
| [FitShape](msdn-online-vml-fitshape-attribute.md)                           | Define si el texto se ajusta a los límites de la forma.                            |
| [Familia de fuentes](msdn-online-vml-font-family-attribute.md)                     | Especifica la familia de fuentes de texto.                                             |
| [Tamaño de fuente](msdn-online-vml-font-size-attribute.md)                         | Especifica el tamaño de fuente del texto.                                               |
| [Estilo de fuente](msdn-online-vml-font-style-attribute.md)                       | Especifica el estilo de fuente del texto.                                              |
| [Font-Variant](msdn-online-vml-font-variant-attribute.md)                   | Especifica la variante de fuente del texto.                                            |
| [Peso de fuente](msdn-online-vml-font-weight-attribute.md)                     | Especifica el grosor de fuente del texto.                                             |
| [Fuente](msdn-online-vml-font-attribute.md)                                   | Especifica el valor de fuente compuesto del texto.                                     |
| [MSO-Text-Shadow](msdn-online-vml-mso-text-shadow-attribute.md)             | Define si se aplica una sombra al texto.                               |
| [Activado](on-attribute--textpath--vml.md)                                        | Define si se muestra el texto.                                         |
| [String](msdn-online-vml-string-attribute.md)                               | Define la cadena de texto.                                                       |
| [Decoración de texto](msdn-online-vml-text-decoration-attribute.md)             | Define la decoración de texto del texto.                                       |
| [Trim](msdn-online-vml-trim-attribute.md)                                   | Define si se quita espacio adicional encima y debajo del texto.               |
| [Letras de rotación de V](msdn-online-vml-v-rotate-letters-attribute.md)           | Determina si se giran las letras del texto.                        |
| [V-Same-Letter-Heights](msdn-online-vml-v-same-letter-heights-attribute.md) | Determina si todas las letras tendrán el mismo alto.                      |
| [V-Text-Align](msdn-online-vml-v-text-align-attribute.md)                   | Define la alineación del texto.                                             |
| [V-Text-Kern](msdn-online-vml-v-text-kern-attribute.md)                     | Determina si el kerning está activado.                                       |
| [V-Text-Reverse](msdn-online-vml-v-text-reverse-attribute.md)               | Determina si se invierte el orden de diseño de las filas.                       |
| [Modo de espaciado de texto en V](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Define el modo para elpacing de letras.                                            |
| [Espaciado de texto en V](msdn-online-vml-v-text-spacing-attribute.md)               | Define la cantidad de espaciado para el texto.                                        |
| [Xscale](msdn-online-vml-xscale-attribute.md)                               | Determina si se usará una ruta de texto recta en lugar de la ruta de acceso de forma. |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

Además de los atributos normales de relleno, cadena y estilo, el atributo [TextPathOK](msdn-online-vml-textpathok-attribute.md) de [Path](msdn-online-vml-path-element.md) debe establecerse en **True** y el atributo [On](on-attribute--textpath--vml.md) de TextPath debe establecerse en **True** para mostrar texto en una ruta de texto.

A continuación se muestra el código mínimo necesario para mostrar texto en una ruta de acceso.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**Ejemplos**

-   [Ejemplo simple de TextPath](/previous-versions/bb264038(v=vs.85))
-   [Ejemplo de tipo de letra TextPath dinámico](/previous-versions/bb264042(v=vs.85))
-   [Ejemplo de curva TextPath dinámica](/previous-versions/bb264041(v=vs.85))

 

 