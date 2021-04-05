---
title: Atributo Focus de VML
description: Atributo Focus de VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078347"
---
# <a name="vml-focus-attribute"></a>Atributo Focus de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el centro de un relleno de degradado lineal. Lectura/escritura **VgFraction**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* Focus = " *expresión* " >

**Sintaxis de script**

*Element* . Focus = "*expresión*"

*expresión* = de *elemento*. Focus

**Comentarios:**

Define la posición inicial del centro de la mezcla. Los valores van del 100% a-100%. El valor predeterminado es 0. Un valor de 100% (o-100%) desplazará el foco para que la dirección de la mezcla se revierta (en efecto, el **color** y el **color2**). Un valor de 50% cambiará la mezcla para que el **color** esté en ambos extremos y el **color2** esté en el centro. Un valor de-50% cambiará la mezcla para que **color2** esté en ambos extremos y el **color** esté en el medio.

*Atributo estándar de VML*

**Ejemplo**

El foco de degradado del relleno se desplaza para que el rojo (**color**) sea una banda en el centro de la forma y que la parte superior e inferior sean azules (**color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 