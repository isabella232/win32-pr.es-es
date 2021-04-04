---
title: Usar el elemento formulas
description: Usar el elemento formulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, fórmulas (elemento)
- diseñar páginas web, elemento de fórmulas
- Lenguaje de marcado de vectores (VML), elemento formulas
- VML (Lenguaje de marcado de vectores), elemento de fórmulas
- graphics Vector, elemento formulas
- elemento formulas
- Elementos VML, fórmulas
- Formas VML, elemento fórmulas
- Lenguaje de marcado de vectores (VML), definir rutas de acceso para las formas
- VML (Lenguaje de marcado de vectores), definir rutas de acceso para las formas
- gráficos vectoriales, definir rutas de acceso para las formas
- Formas VML, definir rutas de acceso
- definir rutas de acceso para las formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077811"
---
# <a name="using-the-formulas-element"></a>Usar el elemento formulas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo usar el `<formulas>` subelemento para definir una ruta de acceso ajustable para una forma.

Puede colocar el <formulas> subelemento dentro `<shape>` `<shapetype>` de o para definir fórmulas que puedan variar la ruta de acceso de una forma. Dentro del `<formulas>` subelemento, un subelemento de **f** define una fórmula para que se evalúe un valor en función de esa fórmula. Por ejemplo, la fórmula `<v:f eqn="prod 10 4 5"/>` define un valor equivalente a "10 x 4/5".

Puede colocar muchos subelementos de **f** dentro de un `<formulas>` subelemento. Las fórmulas pueden hacer referencia a los valores definidos anteriormente en otras fórmulas en el mismo `<formulas>` subelemento. El valor que se define en la primera fórmula se puede conocer como @0 , el valor que se define en la segunda fórmula se puede conocer como @1 , y así sucesivamente.

Además, puede especificar el atributo de la propiedad **ADJ** del `<shape>` elemento, como ADJ = "100, 200, 150". Dentro del `<formulas>` elemento, puede hacer referencia a esos valores en la  lista de ajuste. Se puede hacer referencia al primer valor (100) de **la lista de** ajuste como \# 0, el segundo valor (200) puede denominarse \# 1, etc.

Por ejemplo, para dibujar una esfera sonriente, puede escribir la siguiente representación VML:

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
-   La primera fórmula, `<v:f eqn="sum 33030 0 #0"/>` , define el valor (= 33030 + 0- \# 0). Se puede hacer referencia a este valor como @0 .
-   La segunda fórmula, `<v:f eqn="prod #0 4 3"/>` , define el valor (= \# 0 \* 4/3). Se puede hacer referencia a este valor como @1 .
-   La tercera fórmula, `<v:f eqn="prod @0 1 3"/>` , define el valor (= @0 \* 1/3). Se puede hacer referencia a este valor como @2 .
-   La cuarta fórmula, `<v:f eqn="sum @1 0 @2"/>` , define el valor (= @1 + 0 -@2 ). Se puede hacer referencia a este valor como @3 .
-   Dentro del `<path>` elemento, los valores definidos en las @0 fórmulas primero () y cuarto ( @3 ) se usan para determinar el contorno de la forma.

Si **cambia la lista de ajuste** , como `adj="20000"` , se cambiarán también los valores de las fórmulas que hacen referencia a la lista **de ajuste** , lo que afectará a la superficie sonriente como se indica a continuación:

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





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 