---
title: ADJ (atributo)
description: ADJ (atributo)
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676408"
---
# <a name="adj-attribute"></a>ADJ (atributo)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica un valor de ajuste que se usa para definir los valores de una fórmula. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* ADJ = " *expresión* " >

**Sintaxis de script**

*Element* . ADJ = "*expresión*"

*expresión* = de *elemento*. ADJ

**Comentarios:**

**ADJ** se utiliza para proporcionar puntos ajustables para una fórmula. Si se usa en etiquetas, **ADJ** es una cadena delimitada por comas de hasta 8 valores. Algunos valores se pueden omitir. Por ejemplo, "0, 1, 2, 4, 5, 7" sería una cadena válida pero la cuarta y la séptima parte de los elementos no tendrían valores (los elementos se cuentan a partir de 0).

En el caso de scripting, **ADJ** usa el tipo de datos [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .

*Atributo estándar de VML*

**Vea también**

[Fórmula](msdn-online-vml-formulas-element.md)

**Ejemplo**

Se crea un cuadrado simple con ajustes. En primer lugar, se crea la cadena de **ajust** para definir ocho valores de ajuste. A continuación, se hace referencia a cada valor de ajuste en una de las ocho fórmulas, con cada valor de ajuste precedido por un signo de número ( \# ). Por último, una ruta de acceso se define mediante una cadena que hace referencia a las fórmulas, con cada fórmula precedida por el símbolo de arroba (@).


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



[Ejemplo del atributo ADJ](/previous-versions/bb229662(v=vs.85)) (requiere Microsoft Internet Explorer 5 o posterior).

 

 