---
title: Atributo de ángulo (relleno) (VML)
description: Atributo de ángulo (relleno) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078280"
---
# <a name="angle-attribute-fillvml"></a>Atributo de ángulo (relleno) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el ángulo de un relleno de degradado. Lectura/escritura [VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* Angle = " *expresión* " >

**Sintaxis de script**

*Element* . Angle = "*expresión*"

*expresión* = de *elemento*. Angle

**Comentarios:**

El vector de un degradado es perpendicular al vector de la dirección de combinación de un color a otro. El valor predeterminado es 0 (cero) grados, que es un vector horizontal de izquierda a derecha. Los ángulos positivos giran el degradado en sentido contrario a las agujas del reloj.

*Atributo estándar de VML*

**Ejemplo**

El relleno de la forma se compone de un degradado de dos colores, que se ejecuta de azul a rojo a un ángulo de 45 grados. El color rojo estará en la esquina superior izquierda y el azul estará en la esquina inferior derecha.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 