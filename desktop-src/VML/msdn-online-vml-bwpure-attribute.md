---
title: Atributo BWPure de VML
description: Atributo BWPure de VML
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b06c53ddc6279d16eeeaaed40a87794a1ab06d8b282ce4eef12a0e1bd74e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999305"
---
# <a name="vml-bwpure-attribute"></a>Atributo BWPure de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el modo en blanco y negro para los dispositivos de salida en blanco y negro puros. Lectura/escritura [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:bwpure=" *expression* ">

**Comentarios:**

Cuando [BWMode](msdn-online-vml-bwmode-attribute.md) se establece en **auto**, este atributo se usa para determinar cómo representar la forma en blanco y negro puro.

Para obtener más información acerca de los valores de este atributo, vea el tema [DeCkWhiteMode.](msdn-online-vml-vgblackwhitemode.md) El valor predeterminado es **auto.**

*Microsoft Office Atributo Extensions*

**Ejemplo**

La forma se procesa como una imagen de contraste alto para la salida pura en blanco y negro.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 