---
title: En atributo (sombra) (VML)
description: En atributo (sombra) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995463"
---
# <a name="on-attribute-shadowvml"></a>En atributo (sombra) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará una sombra. Lectura/escritura **VgTriState**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *Element* on = " *expresión* " >

**Sintaxis de script**

*Element* . on = "*expresión*"

*expresión* = de *elemento*. on

**Comentarios:**

Si **es true**, se mostrará la sombra. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

Se mostrará la sombra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 