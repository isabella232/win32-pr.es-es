---
title: EXT (atributo) (sesgo) (VML)
description: EXT (atributo) (sesgo) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271296"
---
# <a name="ext-attribute-skewvml"></a>EXT (atributo) (sesgo) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la forma en que se muestra un sesgo. Lectura/escritura **Cadena**.

**Se aplica a**

[Sesgar](msdn-online-vml-skew-element.md)

**Sintaxis de etiquetas**

<o: *elemento* v:EXT = " *expresión* " >

**Sintaxis de script**

*Element* . ext = "*expresión*"

*expresión* = de *elemento*. ext

**Comentarios:**

Este atributo se utiliza para indicar a los Editores gráficos cómo procesar el elemento de **sesgo** . Estos valores incluyen:

-   **edit**
-   **vista** (valor predeterminado)
-   **backwardCompatible**

Si una extensión está establecida en **Editar**, puede ser omitida por un visor de software. Si se establece en **Ver**, el visor debe representar la representación del mapa de bits en su lugar.

*Microsoft Office atributo Extensions*

 

 