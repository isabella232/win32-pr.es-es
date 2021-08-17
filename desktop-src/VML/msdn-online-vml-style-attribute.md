---
title: Atributo de estilo VML
description: Atributo de estilo VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0b7ce7985687d560fc46ebb98d41b51e7a461e811deb228b0a5709a35c5d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475195"
---
# <a name="vml-style-attribute"></a>Atributo de estilo VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el estilo del marco. Lectura/escritura **Cadena**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *element* style=" *expression* ">

**Sintaxis de script**

*element* .style="*expression*"

*expresión* = *elemento*.style

**Comentarios:**

Este atributo usa los atributos de estilo CSS normales para el posicionamiento.

*Atributo estándar de VML*

**Ejemplo**

El estilo define la posición real del marco.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 