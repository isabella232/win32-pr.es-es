---
title: Atributo angle (Fill)(VML)
description: Atributo angle (Fill)(VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aff7b330d11c95c39176d9cdcd42a839a03a6283fca706cfbc913314ea03b47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864265"
---
# <a name="angle-attribute-fillvml"></a>Atributo angle (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el ángulo de un relleno de degradado. Lectura/escritura [Dvsangle .](msdn-online-vml-vgangleindegrees-data-type.md)

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* angle=" *expression* ">

**Sintaxis de script**

*element* .angle="*expression*"

*expresión* = *elemento*.angle

**Comentarios:**

El vector de un degradado es gradiente al vector de la dirección de mezcla de un color a otro. El valor predeterminado es 0 (cero) grados, que es un vector horizontal de izquierda a derecha. Los ángulos positivos giran el degradado en sentido contrario a las agujas del reloj.

*Atributo estándar de VML*

**Ejemplo**

El relleno de la forma se compone de un degradado de dos colores, que se ejecuta de azul a rojo en un ángulo de 45 grados. Rojo estará en la esquina superior izquierda y azul en la esquina inferior derecha.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 