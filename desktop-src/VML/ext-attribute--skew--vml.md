---
title: Atributo Ext (skew)(VML)
description: Atributo Ext (skew)(VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a001812a5504940509fac82333b2ca637ae76a913218f44cd3a06b4c18bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125365"
---
# <a name="ext-attribute-skewvml"></a>Atributo Ext (skew)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la forma en que se muestra un sesgo. Lectura/escritura **Cadena**.

**Se aplica a**

[Sesgar](msdn-online-vml-skew-element.md)

**Sintaxis de etiquetas**

<o: *elemento* v:ext=" *expresión* ">

**Sintaxis de script**

*element* .ext="*expression*"

*expresión* = *elemento*.ext

**Comentarios:**

Este atributo se usa para decir a los editores gráficos cómo procesar el **elemento Skew.** Estos valores incluyen:

-   **edit**
-   **view** (valor predeterminado)
-   **backwardCompatible**

Si se establece una extensión para **editar**, un visor de software puede omitirla. Si se establece para **ver**, el visor debe representar la representación de mapa de bits en su lugar.

*Microsoft Office Atributo Extensions*

 

 