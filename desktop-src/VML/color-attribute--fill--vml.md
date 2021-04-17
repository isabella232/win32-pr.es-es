---
title: Atributo de color (relleno) (VML)
description: Atributo de color (relleno) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487774"
---
# <a name="color-attribute-fillvml"></a>Atributo de color (relleno) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el color de un relleno. Lectura/escritura **VgColor**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* color = " *expresión* " >

**Sintaxis de script**

*Element* . color = "*expresión*"

*expresión* = de *elemento*. color

**Comentarios:**

Invalida el atributo **fillColor** de una forma. El valor predeterminado es **blanco**.

*Atributo estándar de VML*

**Ejemplo**

El color de relleno de la forma es verde.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 