---
title: Atributo de atribución VML
description: Atributo de atribución VML
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359382"
---
# <a name="vml-endangle-attribute"></a>Atributo de atribución VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el extremo del arco. Lectura/escritura. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .

**Se aplica a**

[Arc](msdn-online-vml-arc-element.md)

**Sintaxis de etiquetas**

<v: *elemento* dependiente = " *expresión* " >

**Sintaxis de script**

*elemento* . impuesto = "*expresión*"

*expresión* = de *elemento*. impuesto

**Comentarios:**

El arco se define como un trazo dibujado a lo largo de un óvalo limitado por los atributos de **estilo** de una forma. El final del trazo se define mediante un ángulo medido desde la derecha hacia arriba (12 en la izquierda). El valor predeterminado es 90 grados.

*Atributo estándar de VML*

**Ejemplo**

El arco es sonriente. El punto de inicio se encuentra en el punto de 90 de una elipse inscrita dentro del cuadro de límite de la forma. El punto final se encuentra en el punto de 270 grados del óvalo.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 