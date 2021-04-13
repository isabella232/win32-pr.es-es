---
title: Atributo de tipo (sombra) (VML)
description: Atributo de tipo (sombra) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421062"
---
# <a name="type-attribute-shadowvml"></a>Atributo de tipo (sombra) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica el tipo de sombra. Lectura/escritura **Cadena**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *Element* Type = " *expresión* " >

**Sintaxis de script**

*Element* . Type = "*expresión*"

*expresión* = de *elemento*. Type

**Comentarios:**

Estos valores incluyen:



| Value           | Descripción                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sola          | Sombra única. Predeterminada.                                                                                                                                                                              |
| double          | Sombra doble. [Color2](color2-attribute--shadow--vml.md) se usa para el color de la segunda sombra y se usa [Offset2](msdn-online-vml-offset2-attribute.md) para el desplazamiento de la segunda sombra. |
| perspectiva     | Sombra de perspectiva.                                                                                                                                                                                |
| shapeRelative   | La sombra se crea en relación con la forma.                                                                                                                                                         |
| drawingRelative | La sombra se crea en relación con el dibujo.                                                                                                                                                       |
| relieve          | La sombra tiene una apariencia en relieve.                                                                                                                                                                     |



 

**Atributo estándar de VML**

**Ejemplo**

Se crea una sombra doble con la segunda sombra verde y desplazamiento 5 puntos hacia abajo y hacia la derecha.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 