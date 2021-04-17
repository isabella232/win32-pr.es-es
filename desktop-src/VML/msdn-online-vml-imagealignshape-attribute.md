---
title: Atributo ImageAlignShape de VML
description: Atributo ImageAlignShape de VML
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359135"
---
# <a name="vml-imagealignshape-attribute"></a>Atributo ImageAlignShape de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina la alineación de la imagen del trazo. Lectura/escritura **VgTriState**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v:

Element *imagealignshape = "* expresión *" >*

**Sintaxis de script**

Element *. imagealignshape = "* expresión *"*

*=* elemento Expression *. imagealignshape*

**Comentarios:**

Si **es true**, alinea la imagen con la forma, de lo contrario, la imagen se alinea con la ventana. El valor predeterminado es **True**.

*Atributo estándar de VML*

**Ejemplo**

La imagen se alinea con la ventana.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 