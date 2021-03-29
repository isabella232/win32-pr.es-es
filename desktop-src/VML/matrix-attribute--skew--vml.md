---
title: Matrix (atributo) (sesgo) (VML)
description: Matrix (atributo) (sesgo) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078276"
---
# <a name="matrix-attribute-skewvml"></a>Matrix (atributo) (sesgo) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una transformación de perspectiva de un sesgo. Lectura/escritura **Cadena**.

**Se aplica a**

[Sesgar](msdn-online-vml-skew-element.md)

**Sintaxis de etiquetas**

<o: *elemento* Matrix = " *expresión* " >

**Sintaxis de script**

*Element* . Matrix = "*expresión*"

*expresión* = de *elemento*. Matrix

**Comentarios:**

La matriz es una cadena con el formato "SXX, SXY, SYX, SYY, PX, py", donde s es Scale, p es Perspective y x e y son valores x e y. Si el [desplazamiento](offset-attribute--skew--vml.md) está en unidades absolutas, PX y py están en [unidades](msdn-online-vml-units.md) de la UME ^-1 (de lo contrario, son una fracción inversa del tamaño de la forma). El valor predeterminado es "1, 0, 0, 1, 0".

*Microsoft Office atributo Extensions*

 

 