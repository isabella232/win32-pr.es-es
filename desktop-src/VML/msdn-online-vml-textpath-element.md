---
title: Elemento TextPath de VML
description: Elemento TextPath de VML
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676383"
---
# <a name="vml-textpath-element"></a>Elemento TextPath de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una ruta de acceso de texto para una forma.

Los atributos siguientes modifican una ruta de acceso de texto.



| Atributo                                                                    | Descripción                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FitPath](msdn-online-vml-fitpath-attribute.md)                             | Define si el texto se ajusta a la ruta de acceso de una forma.                             |
| [FitShape](msdn-online-vml-fitshape-attribute.md)                           | Define si el texto se ajusta a los límites de la forma.                            |
| [Familia de fuentes](msdn-online-vml-font-family-attribute.md)                     | Especifica la familia de fuentes de texto.                                             |
| [Tamaño de fuente](msdn-online-vml-font-size-attribute.md)                         | Especifica el tamaño de fuente del texto.                                               |
| [Estilo de fuente](msdn-online-vml-font-style-attribute.md)                       | Especifica el estilo de fuente del texto.                                              |
| [Font-variante](msdn-online-vml-font-variant-attribute.md)                   | Especifica la variante de fuente del texto.                                            |
| [Espesor de fuente](msdn-online-vml-font-weight-attribute.md)                     | Especifica el peso de la fuente del texto.                                             |
| [Fuente](msdn-online-vml-font-attribute.md)                                   | Especifica el valor de la fuente compuesta del texto.                                     |
| [MSO-texto-sombra](msdn-online-vml-mso-text-shadow-attribute.md)             | Define si se aplica una sombra al texto.                               |
| [Activado](on-attribute--textpath--vml.md)                                        | Define si se muestra el texto.                                         |
| [String](msdn-online-vml-string-attribute.md)                               | Define la cadena de texto.                                                       |
| [Decoración de texto](msdn-online-vml-text-decoration-attribute.md)             | Define la decoración de texto del texto.                                       |
| [Trim](msdn-online-vml-trim-attribute.md)                                   | Define si se quita el espacio adicional por encima y por debajo del texto.               |
| [V-Rotate-Letras](msdn-online-vml-v-rotate-letters-attribute.md)           | Determina si las letras del texto se giran.                        |
| [V-Same-letra-alto](msdn-online-vml-v-same-letter-heights-attribute.md) | Determina si todas las letras tendrán el mismo alto.                      |
| [Alineación de texto V](msdn-online-vml-v-text-align-attribute.md)                   | Define la alineación del texto.                                             |
| [Texto V-kerning](msdn-online-vml-v-text-kern-attribute.md)                     | Determina si el kerning está activado.                                       |
| [Texto V: inverso](msdn-online-vml-v-text-reverse-attribute.md)               | Determina si se invierte el orden de diseño de las filas.                       |
| [Modo de espaciado de texto V](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Define el modo de espaciado entre letras.                                            |
| [Espaciado de texto V](msdn-online-vml-v-text-spacing-attribute.md)               | Define la cantidad de espaciado del texto.                                        |
| [XScale](msdn-online-vml-xscale-attribute.md)                               | Determina si se utilizará un textpath recto en lugar de la ruta de acceso de la forma. |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

Además de los atributos normales de relleno, cadena y estilo, el atributo [TextPathOK](msdn-online-vml-textpathok-attribute.md) de [path](msdn-online-vml-path-element.md) debe establecerse en **true** y el atributo [on](on-attribute--textpath--vml.md) de TextPath debe establecerse en **true** para mostrar el texto en una ruta de acceso de texto.

A continuación se muestra el código mínimo necesario para mostrar texto en un trazado.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**Ejemplos**

-   [Ejemplo de TextPath simple](/previous-versions/bb264038(v=vs.85))
-   [Ejemplo de tipo de letra de TextPath dinámico](/previous-versions/bb264042(v=vs.85))
-   [Ejemplo de curva TextPath dinámica](/previous-versions/bb264041(v=vs.85))

 

 