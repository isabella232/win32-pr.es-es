---
title: Atributo MSO-Wrap-Mode de VML
description: Atributo MSO-Wrap-Mode de VML
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e3743522b9286da8a7f30e9100e06205430b1b18fa3c62def60b57f54b65d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136988"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Atributo MSO-Wrap-Mode de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el modo de ajuste del texto. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="mso-wrap-mode: *expression* ">

**Comentarios:**

Estos valores incluyen:



| Value          | Descripción                          |
|----------------|--------------------------------------|
| square         | Ajusta el texto alrededor de la forma en un cuadrado. |
| Apretado          | El texto se ajusta cerca de la forma.  |
| superior e inferior | El texto salta de arriba abajo.       |
| a través de        | El texto se muestra a través de la forma.     |
| ninguno           | El texto no se ajusta.                   |



 

Usado por Microsoft PowerPoint para guardar en HTML para indicar si el ajuste de palabras dentro de una autoforma está en **(** cuadrado ) o desactivado (**ninguno**).

*Microsoft Office Atributo Extensions*

**Ejemplo**

El código siguiente indica que el ajuste de texto dentro de una autoforma está activado en PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 