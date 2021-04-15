---
title: Atributo FitShape de VML
description: Atributo FitShape de VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676505"
---
# <a name="vml-fitshape-attribute"></a>Atributo FitShape de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define si el texto se ajusta al rectángulo de selección de una forma. Lectura/escritura **VgTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* fitshape = " *expresión* " >

**Sintaxis de script**

*Element* . fitshape = "*expresión*"

*expresión* = de *elemento*. fitshape

**Comentarios:**

Si **es true**, ajusta el texto a los bordes del cuadro que define la forma completa. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

El texto se ajustará para ajustarse a la forma.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 