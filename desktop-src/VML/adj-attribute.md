---
title: Atributo Adj
description: Atributo Adj
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85869500cc3e9f86e0f48e67f63cfd9e6ed2cff5580caa04994169a9e4b50df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137148"
---
# <a name="adj-attribute"></a>Atributo Adj

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica un valor de ajuste utilizado para definir los valores de una fórmula. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* adj=" *expression* ">

**Sintaxis de script**

*element* .adj="*expression*"

*expresión* = *elemento*.adj

**Comentarios:**

**Adj** se usa para proporcionar puntos ajustables para una fórmula. Si se usa en etiquetas, **Adj** es una cadena delimitada por comas de hasta 8 valores. Se pueden omitir algunos valores. Por ejemplo, "0,1,2,,4,5,7" sería una cadena válida, pero el cuarto y el séptimo elemento no tendrían valores (los elementos se cuentan a partir de 0).

Para el scripting, **Adj** usa el tipo de datos [IVgAdjustments.](msdn-online-vml-ivgadjustments-data-type.md)

*Atributo estándar de VML*

**Vea también**

[Fórmula](msdn-online-vml-formulas-element.md)

**Ejemplo**

Se crea un cuadrado simple con ajustes. En primer **lugar, se** crea la cadena Adj para definir ocho valores de ajuste. A continuación, una de las ocho fórmulas hace referencia a cada valor de ajuste, con cada valor de ajuste precisado por un símbolo de signo de número ( \# ). Por último, una ruta de acceso se define mediante una cadena que hace referencia a las fórmulas, con cada fórmula precarizada por el símbolo de signo "at" (@).


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



[Ejemplo de atributo Adj](/previous-versions/bb229662(v=vs.85)) (requiere Microsoft Internet Explorer 5 o superior).

 

 