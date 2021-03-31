---
title: Atributo TextPathOK de VML
description: Atributo TextPathOK de VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904628"
---
# <a name="vml-textpathok-attribute"></a>Atributo TextPathOK de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará una ruta de acceso de texto. Lectura/escritura **VgTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *Element* textpathok = " *expresión* " >

**Sintaxis de script**

*elemento* . textpathok = "*expresión*"

*expresión* = de *elemento*. textpathok

**Comentarios:**

Si **es false**, la ruta de acceso no puede tener una ruta de acceso de texto. El valor predeterminado es **False**. Debe tener este atributo establecido en **true** para mostrar texto en una ruta de acceso.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene una ruta de acceso de texto. El texto "Hola VML" se muestra a lo largo de una curva en forma de sonrisa.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 