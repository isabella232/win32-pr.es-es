---
title: Usar el elemento Formulas
description: Usar el elemento Formulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Taller web, elemento formulas
- diseñar páginas web, elemento formulas
- Lenguaje de marcado de vectores (VML),elemento formulas
- VML (Lenguaje de marcado de vectores),elemento formulas
- vector graphics,formulas element
- elemento formulas
- Elementos de VML, fórmulas
- VmL shapes,formulas element
- Lenguaje de marcado de vectores (VML), definir rutas de acceso para las formas
- VML (Lenguaje de marcado de vectores), definir rutas de acceso para las formas
- gráficos vectoriales, definición de rutas de acceso para formas
- Formas de VML, definir rutas de acceso
- definir rutas de acceso para formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23810ae6612e18132566c7d546db7f1f3a569871050b7919cbd8512f3d832808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512809"
---
# <a name="using-the-formulas-element"></a>Usar el elemento Formulas

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, se ilustrará cómo usar el sub elemento para definir una ruta `<formulas>` de acceso ajustable para una forma.

Puede colocar el <formulas> sub elemento dentro de o para definir `<shape>` `<shapetype>` fórmulas que pueden variar el trazado de una forma. Dentro del sub element, un sub element f define una fórmula para que un valor se evalúe `<formulas>` en función de esa fórmula.  Por ejemplo, la fórmula define `<v:f eqn="prod 10 4 5"/>` un valor equivalente a "10 x 4/5".

Puede colocar muchos sub-elementos **f** dentro de `<formulas>` un sub-elemento. Las fórmulas pueden hacer referencia a los valores definidos anteriormente en otras fórmulas dentro del mismo `<formulas>` sub element. El valor que se define en la primera fórmula se puede hacer referencia a como , el valor que se define en la segunda fórmula se puede hacer referencia a como , y @0 @1 así sucesivamente.

Además, puede especificar el atributo de propiedad **adj** del elemento, como `<shape>` adj="100, 200, 150". Dentro del `<formulas>` elemento , puede hacer referencia a esos valores en la lista **adj.** El primer valor (100) de la lista **adj** se puede denominar 0, el segundo valor (200) se puede hacer referencia a como 1, y así \# \# sucesivamente.

Por ejemplo, para dibujar una cara sonriente, puede escribir la siguiente representación de VML:

![shape1.gif (735 bytes)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   `adj="17520"` define un valor (= 17520). Se puede hacer referencia a este valor como \# 0.
-   La primera fórmula, `<v:f eqn="sum 33030 0 #0"/>` , define el valor (= 33030 + 0 - \# 0). Se puede hacer referencia a este valor como @0 .
-   La segunda fórmula, `<v:f eqn="prod #0 4 3"/>` , define el valor (= \# 0 \* 4/3). Se puede hacer referencia a este valor como @1 .
-   La tercera fórmula, `<v:f eqn="prod @0 1 3"/>` , define el valor (= @0 \* 1 /3). Se puede hacer referencia a este valor como @2 .
-   La cuarta fórmula, `<v:f eqn="sum @1 0 @2"/>` , define el valor (= + @1 0 -@2 ). Se puede hacer referencia a este valor como @3 .
-   Dentro del elemento , los valores definidos en las fórmulas first ( ) y fourth ( ) se usan para determinar el `<path>` @0 contorno de la @3 forma.

Si cambia la **lista de ad,** como , los valores de las fórmulas que hacen referencia a la lista de ad también se cambiarán, lo que afectará a la cara sonriente como se muestra a `adj="20000"` continuación: 

![shape2.gif (765 bytes)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





Para obtener más información sobre este elemento, consulte la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 