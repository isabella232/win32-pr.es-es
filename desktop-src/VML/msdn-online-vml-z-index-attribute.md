---
title: Atributo Z-Index de VML
description: Atributo Z-Index de VML
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07100b2ecdbda792ea3f7d5550759430539b95b86c5ef76ded2f9238785b1151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123775"
---
# <a name="vml-z-index-attribute"></a>Atributo Z-Index de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina el orden de presentación de las formas superpuestas. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="z-index: *expression* ">

**Sintaxis de script**

*element* .style.zindex="*expression*"

*expresión* = *elemento*.style.zindex

**Comentarios:**

El **atributo Z-Index** es similar al atributo HTML **Z-Index estándar** para los estilos.

Estos valores incluyen:



| Value | Descripción                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto  | Se usará el orden en que las formas aparecen en la página HTML, de abajo a arriba.                                                                                                                         |
| orden | Número que representa la precedencia de apilamiento. Una forma con un número más alto se mostrará como si estuviera sobresaliendo (en "delante" de) una forma con un número inferior. Se pueden usar números negativos. |



 

*Atributo estándar de VML*

**Ejemplo**

La forma roja se mostrará en la "parte delantera" de la forma azul, porque tiene un índice z superior.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Ejemplo de atributo Z-Index](/previous-versions/ms530275(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 