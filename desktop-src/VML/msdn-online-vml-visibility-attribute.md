---
title: Atributo de visibilidad de VML
description: Atributo de visibilidad de VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695654"
---
# <a name="vml-visibility-attribute"></a>Atributo de visibilidad de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se muestra una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* style = "Visibility: *Expression* " >

**Sintaxis de script**

*Element* . Style. Visibility = "*expresión*"

*expresión* = de *elemento*. Style. Visibility

**Comentarios:**

El atributo **Visibility** es similar al atributo de **visibilidad** HTML estándar para los estilos.

Estos valores incluyen:



| Value    | Descripción                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | La forma está visible.                                                                                                                                                                   |
| hidden   | La forma no es visible, pero sigue siendo parte del flujo de los objetos en el explorador. No se procesan los eventos del mouse.                                                                  |
| inherit  | Predeterminada. El estado de visibilidad se hereda del elemento primario de la forma. Las aplicaciones de Microsoft Office solo utilizan **inherit** y **Hidden**. los demás valores se asignan a **inherit**. |
| contraer | Se usa para aplicaciones de edición gráficas que pueden contraer grupos de formas. por ejemplo, los esquemas.                                                                                     |



 

*Atributo estándar de VML*

**Ejemplo**

En el código siguiente se crea una forma, pero se oculta. Otros objetos del documento fluyen alrededor de él, lo que deja un espacio del mismo tamaño que la forma.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Ejemplo de atributo de visibilidad](/previous-versions/bb264100(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 