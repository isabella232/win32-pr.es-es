---
title: Usar el elemento handles
description: Usar el elemento handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web Workshop, Controls (elemento)
- diseñar páginas web, elemento handles
- Lenguaje de marcado de vectores (VML), elemento handles
- VML (Lenguaje de marcado de vectores), elemento handles
- Vector Graphics, elemento handles
- Controls (elemento)
- Elementos VML, identificadores
- Formas VML, elemento handles
- Lenguaje de marcado de vectores (VML), adjuntar texto a formas
- VML (Lenguaje de marcado de vectores), adjuntar texto a formas
- gráficos vectoriales, adjuntar texto a formas
- Formas VML, adjuntar texto
- Adjuntar texto a formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077810"
---
# <a name="using-the-handles-element"></a>Usar el elemento handles

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo usar el `<handles>` elemento para adjuntar texto a una forma.

Puede colocar el `<handles>` subelemento dentro de `<shape>` o `<shapetype>` para definir los elementos de la interfaz de usuario que  pueden variar los valores de ajuste de la forma.

Por ejemplo, como se muestra en la siguiente representación VML, puede proporcionar un controlador de ajuste (cuadro amarillo) que los usuarios simplemente pueden arrastrar para ajustar la forma.

Nota: los controladores están disponibles cuando se ve esta forma VML en Microsoft Office aplicaciones, donde la forma está pensada para ser manipulable.

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





Observe que la única diferencia entre la representación de VML anterior **y la siguiente es el valor de** ajuste.

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





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 