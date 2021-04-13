---
title: Atributo de ganancia de VML
description: Atributo de ganancia de VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421068"
---
# <a name="vml-gain-attribute"></a>Atributo de ganancia de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la intensidad de todos los colores de una imagen. Lectura/escritura **VgNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *elemento* ganancia = " *expresión* " >

**Sintaxis de script**

*Element* . beneficio = "*expresión*"

*expresión* = de *elemento*. ganancia

**Comentarios:**

Este atributo define la luminosidad del color blanco, lo que afecta a todos los demás colores. Los valores oscilan entre 0 y infinito. El valor predeterminado es 1,0. Un valor de 0 no muestra ninguna imagen. Los valores mayores que 1 aclaran la imagen y los valores inferiores a 1 hacen que la imagen parezca Grayer.

Este atributo se puede usar para crear efectos interesantes.

*Atributo estándar de VML*

**Ejemplo**

La imagen se mostrará con todos los colores que tienden a atenuar.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 