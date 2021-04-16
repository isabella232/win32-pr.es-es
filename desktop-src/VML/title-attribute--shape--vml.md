---
title: Título (forma) (VML)
description: Título (forma) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488239"
---
# <a name="title-attribute-shapevml"></a>Título (forma) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* title = " *expresión* " >

**Sintaxis de script**

*Element* . title = "*expresión*"

*expresión* = de *elemento*. title

**Comentarios:**

El atributo **title** es similar al atributo **title** de HTML estándar. El comportamiento de un título es similar a la información sobre herramientas de Microsoft Windows.

**Atributo estándar de VML**

**Ejemplo**

El título de la forma es "visualización de la información sobre herramientas" y aparecerá cuando el puntero del mouse se mueva sobre la forma.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo de título](/previous-versions/bb264097(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 