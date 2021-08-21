---
title: Usar el elemento Textpath
description: Usar el elemento Textpath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Taller web, elemento textpath
- diseñar páginas web, elemento textpath
- Lenguaje de marcado de vectores (VML),elemento textpath
- VML (Lenguaje de marcado de vectores),elemento textpath
- gráficos vectoriales, elemento textpath
- elemento textpath
- Elementos VML,textpath
- Formas de VML, elemento textpath
- Lenguaje de marcado de vectores (VML), dibujar texto
- VML (Lenguaje de marcado de vectores), dibujar texto
- gráficos vectoriales, dibujar texto VML
- dibujar texto
- Formas de VML, dibujar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5db3b76d0c4ad2e56c59cfcf6dd39a2af51317b63ee190f47d794933282b5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056986"
---
# <a name="using-the-textpath-element"></a>Usar el elemento Textpath

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, se ilustrará cómo usar el `<textpath>` elemento para dibujar texto con varios estilos.

Puede colocar el `<textpath>` sub elemento dentro de o para dibujar `<shape>` `<shapetype>` texto. A continuación, puede usar los atributos de propiedad del `<textpath>` sub elemento para personalizar el texto. También puede usar el `<formulas>` sub element para definir el contorno del texto.

Por ejemplo, para crear el texto que se muestra en la siguiente imagen, puede escribir la siguiente representación de VML. Observe que usamos el `<shapetype>` elemento para definir un prototipo para el esquema del texto. A continuación, creamos una instancia de dos formas a partir del mismo tipo de forma. Simplemente puede cambiar el atributo **de propiedad de** cadena para mostrar texto diferente.

![shape1 \-1.gif (4898 bytes)](images/shape1-1t.gif)

![shape1 \-2.gif (2789 bytes)](images/shape1-2t.gif)


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





Para obtener más información sobre este elemento, consulte la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 