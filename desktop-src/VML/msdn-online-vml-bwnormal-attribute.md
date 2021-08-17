---
title: Atributo BWNormal de VML
description: Atributo BWNormal de VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754960"
---
# <a name="vml-bwnormal-attribute"></a>Atributo BWNormal de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el modo en blanco y negro para los dispositivos de salida normales en blanco y negro. Lectura/escritura [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:bwnormal=" *expression* ">

**Comentarios:**

Cuando [BWMode](msdn-online-vml-bwmode-attribute.md) se establece en **auto**, este atributo se usa para determinar cómo representar la forma en blanco y negro normal.

Para obtener más información sobre los valores de este atributo, vea el tema [DeCkBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) El valor predeterminado es **auto.**

*Microsoft Office Atributo Extensions*

**Ejemplo**

La forma se procesa como una imagen de escala de grises para una salida normal en blanco y negro.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 