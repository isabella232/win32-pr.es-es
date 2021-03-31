---
title: Atributo Rotation (forma) (VML)
description: Atributo Rotation (forma) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078318"
---
# <a name="rotation-attribute-shapevml"></a>Atributo Rotation (forma) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el ángulo en el que se gira una forma. Lectura/escritura [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Rotation: *Expression* " >

**Sintaxis de script**

*Element* . Rotation = "*expresión*"

*expresión* = de *elemento*. Rotation

**Comentarios:**

El valor en grados puede ser positivo o negativo, y los valores mayores que 360 se pueden dividir en un círculo de 360 grados. Los ángulos positivos están a la derecha. El valor predeterminado es 0.

Tenga en cuenta que se cambia la posición de la forma después de la rotación para reflejar las nuevas coordenadas del cuadro de límite.

Tenga en cuenta también que para el scripting, no se utiliza el atributo de **estilo** y ese **giro** se trata como un atributo directo de la forma.

El atributo **Rotation** es similar al atributo **rotación** HTML estándar para los estilos.

*Atributo estándar de VML*

**Vea también**

**Ejemplo**

El rectángulo se inclinará 45 grados.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Ejemplo del atributo Rotation](/previous-versions/bb264091(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 