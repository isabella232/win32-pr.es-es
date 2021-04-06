---
title: Atributo BWNormal de VML
description: Atributo BWNormal de VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077960"
---
# <a name="vml-bwnormal-attribute"></a>Atributo BWNormal de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el modo de blanco y negro para los dispositivos de salida normales de color negro y blanco. Lectura/escritura [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* o:bwnormal = " *expresión* " >

**Comentarios:**

Cuando [BWMode](msdn-online-vml-bwmode-attribute.md) se establece en **auto**, este atributo se usa para determinar cómo representar la forma en blanco y negro normales.

Para obtener más información sobre los valores de este atributo, vea el tema [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . El valor predeterminado es **automático**.

*Microsoft Office atributo Extensions*

**Ejemplo**

La forma se procesa como una imagen de escala de grises para la salida normal de blanco y negro.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 