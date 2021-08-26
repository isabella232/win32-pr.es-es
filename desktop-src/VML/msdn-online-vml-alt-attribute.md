---
title: Atributo Alt de VML
description: Atributo Alt de VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08714efca9a390cbbec2f3dcf14782053d34db3506462214b9e62ebf1da206a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905345"
---
# <a name="vml-alt-attribute"></a>Atributo Alt de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el texto alternativo que se va a mostrar en lugar de un gráfico. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* alt=" *expression* ">

**Sintaxis de script**

*element* .alt="*expression*"

*expresión* = *elemento*.alt

**Comentarios:**

El **atributo Alt** es similar al atributo ALT HTML estándar.  Este atributo proporciona una manera para que los exploradores que convierten texto en voz describan los elementos gráficos de una página.

*Atributo estándar de VML*

**Vea también**

[Forma](shape-element--vml.md)

**Ejemplo**

El **elemento Alt** siguiente mostrará la frase "Rectángulo rojo" en los exploradores que convierten las páginas web en frases habladas.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo Alt](/previous-versions/bb229663(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 