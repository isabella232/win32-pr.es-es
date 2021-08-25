---
title: Atributo de matriz (sesgo)(VML)
description: Atributo de matriz (sesgo)(VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7fd3989807951f06df963c6899a2c81ce6e7faaa76432172e4391a4ce11029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768455"
---
# <a name="matrix-attribute-skewvml"></a>Atributo de matriz (sesgo)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una transformación de perspectiva de un sesgo. Lectura/escritura **Cadena**.

**Se aplica a**

[Sesgar](msdn-online-vml-skew-element.md)

**Sintaxis de etiquetas**

<o: *element* matrix=" *expression* ">

**Sintaxis de script**

*element* .matrix="*expression*"

*expresión* = *element*.matrix

**Comentarios:**

La matriz es una cadena con el formato "sxx, sxy, syx, syy, px, py", donde s es scale, p es perspective y x e y son valores x e y. Si [Offset](offset-attribute--skew--vml.md) está en unidades absolutas, px y py están en unidades emu^-1 [](msdn-online-vml-units.md) (de lo contrario, son una fracción inversa del tamaño de la forma). El valor predeterminado es "1,0,0,1,0,0".

*Microsoft Office Atributo Extensions*

 

 