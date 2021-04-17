---
title: Atributo de matriz (sombra) (VML)
description: Atributo de matriz (sombra) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421320"
---
# <a name="matrix-attribute-shadowvml"></a>Atributo de matriz (sombra) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una transformación de perspectiva para una sombra. Lectura/escritura **Cadena**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *Element* Matrix = " *expresión* " >

**Sintaxis de script**

*Element* . Matrix = "*expresión*"

*expresión* = de *elemento*. Matrix

**Comentarios:**

Una matriz de transformación de perspectiva con el formato "SXX, SXY, SYX, SYY, PX, py" donde s = scale y p = perspectiva. Si el desplazamiento está en unidades absolutas, PX, py están en unidades de 1/UME; de lo contrario, se trata de una fracción inversa del tamaño de la forma.

*Atributo estándar de VML*

 

 