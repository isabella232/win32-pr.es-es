---
title: Usar el elemento Textpath
description: Usar el elemento Textpath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Web Workshop, elemento textpath
- diseñar páginas web, elemento textpath
- Lenguaje de marcado de vectores (VML), elemento textpath
- VML (Lenguaje de marcado de vectores), elemento textpath
- graphics Vector, elemento textpath
- elemento textpath
- Elementos VML, textpath
- Formas VML, elemento textpath
- Lenguaje de marcado de vectores (VML), dibujar texto
- VML (Lenguaje de marcado de vectores), texto de dibujo
- gráficos vectoriales, dibujar texto VML
- dibujar texto
- Formas VML, texto de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149585"
---
# <a name="using-the-textpath-element"></a>Usar el elemento Textpath

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo usar el `<textpath>` elemento para dibujar texto con varios estilos.

Puede colocar el `<textpath>` subelemento dentro `<shape>` o `<shapetype>` para dibujar el texto. Después, puede usar los atributos de propiedad del `<textpath>` subelemento para personalizar el texto. También puede usar el `<formulas>` subelemento para definir el contorno del texto.

Por ejemplo, para crear el texto que se muestra en la siguiente imagen, puede escribir la representación de VML a continuación. Observe que usamos el `<shapetype>` elemento para definir un prototipo para el contorno del texto. A continuación, se crean instancias de dos formas del mismo TipoForma. Simplemente puede cambiar el atributo de propiedad de **cadena** para mostrar texto diferente.

![\-1.gif shape1 (4898 bytes)](images/shape1-1t.gif)

![\-2.gif shape1 (2789 bytes)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 