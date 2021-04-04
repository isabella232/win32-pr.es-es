---
title: Atributo BWMode de VML
description: Atributo BWMode de VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792370"
---
# <a name="vml-bwmode-attribute"></a>Atributo BWMode de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina cómo se representará una forma para dispositivos de salida en blanco y negro. Lectura/escritura [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* o:bwmode = " *expresión* " >

**Comentarios:**

Cuando una forma se imprime en una impresora de color negro y blanco o se muestra en una vista de color negro y blanco en una aplicación, es posible que haya varias opciones. Para obtener más información sobre los valores de este atributo, vea el tema [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . El valor predeterminado es **automático**.

Si se especifica **auto** , [BWNormal](msdn-online-vml-bwnormal-attribute.md) se usa para determinar el comportamiento de la salida normal de blanco y negro, y [BWPure](msdn-online-vml-bwpure-attribute.md) se usa para determinar el comportamiento de los resultados puros en blanco y negro.

*Microsoft Office atributo Extensions*

**Ejemplo**

El modo de blanco y negro de la forma es **automático**.


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 