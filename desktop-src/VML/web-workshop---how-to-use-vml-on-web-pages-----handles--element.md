---
title: Usar el elemento Handles
description: Usar el elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Taller web, elemento handles
- diseñar páginas web, elemento handles
- Lenguaje de marcado de vectores (VML), elemento handles
- VML (Lenguaje de marcado de vectores), elemento handles
- vector graphics,handles element
- elemento handles
- Elementos de VML, identificadores
- Elemento shapes,handles de VML
- Lenguaje de marcado de vectores (VML), adjuntar texto a formas
- VML (Lenguaje de marcado de vectores), adjuntar texto a formas
- gráficos vectoriales, adjuntar texto a formas
- Formas de VML, adjuntar texto
- adjuntar texto a formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d504024a3d5c42caf8af116a08e5bd8787905991f14c4181fe3a75b10f4814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057217"
---
# <a name="using-the-handles-element"></a>Usar el elemento Handles

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, se ilustrará cómo usar el `<handles>` elemento para adjuntar texto a una forma.

Puede colocar el sub elemento dentro de o para definir elementos de la interfaz de usuario que pueden variar `<handles>` `<shape>` los valores de `<shapetype>` **adj** en la forma.

Por ejemplo, como se muestra en la siguiente representación de VML, puede proporcionar un controlador de ajuste (cuadro amarillo) que los usuarios pueden arrastrar simplemente para ajustar la forma.

Nota: Los identificadores están disponibles cuando esta forma de VML se ve en Microsoft Office aplicaciones, donde la forma está pensada para ser manipulable.

![shape1.gif (564 bytes)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Observe que la única diferencia entre la representación de VML anterior y la siguiente es el **valor adj.**

![shape2.gif (1361 bytes)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Para obtener más información sobre este elemento, consulte la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 