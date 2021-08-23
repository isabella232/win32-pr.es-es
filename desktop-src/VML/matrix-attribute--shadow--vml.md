---
title: Atributo de matriz (Shadow)(VML)
description: Atributo de matriz (Shadow)(VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6124005ef3202e11dc8a4e7eeeaacba8e87e9c3a7cb3a1dd1eee55c595e40ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057933"
---
# <a name="matrix-attribute-shadowvml"></a>Atributo de matriz (Shadow)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una transformación de perspectiva para una sombra. Lectura/escritura **Cadena**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *element* matrix=" *expression* ">

**Sintaxis de script**

*element* .matrix="*expression*"

*expresión* = *element*.matrix

**Comentarios:**

Matriz de transformación de perspectiva con el formato "sxx,sxy,syx,syy,px,py", donde s= scale y p = perspective. Si offset está en unidades absolutas, entonces px, py está en unidades de 1/emu; de lo contrario, son una fracción inversa del tamaño de la forma.

*Atributo estándar de VML*

 

 