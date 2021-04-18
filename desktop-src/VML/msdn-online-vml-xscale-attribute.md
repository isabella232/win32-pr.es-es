---
title: Atributo VML XScale
description: Atributo VML XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359030"
---
# <a name="vml-xscale-attribute"></a>Atributo VML XScale

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se utilizará un textpath recto en lugar de la ruta de acceso de la forma. Lectura/escritura **VgTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "XScale: *expresión* " >

**Sintaxis de script**

*Element* . Style. XScale = "*expresión*"

*expresión* = de *Element*. Style. XScale

**Comentarios:**

Si **es true**, el texto se ejecuta a lo largo de apath de izquierda a derecha a lo largo del valor x del límite inferior de la forma. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

El texto aparecerá como si se dibujara en una línea horizontal, aunque la ruta de la forma sea una diagonal.


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 