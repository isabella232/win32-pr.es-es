---
title: Atributo FillType de VML
description: Atributo FillType de VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0264fe6cd8cd3dfb7592aea25ef855fda01632647b23f0ab2cffe84c4c504918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680805"
---
# <a name="vml-filltype-attribute"></a>Atributo FillType de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tipo de relleno utilizado para el fondo de un trazo. Lectura/escritura **FillFillType**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* filltype=" *expression* ">

**Sintaxis de script**

*element* .filltype="*expression*"

*expresión* = *elemento*.filltype

**Comentarios:**

Estos valores incluyen:



| DashStyle | Descripción                                    |
|-----------|------------------------------------------------|
| Sólido     | El patrón de relleno es sólido. Valor predeterminado.      |
| Tile      | La imagen de relleno está en mosaico.                       |
| Patrón   | La imagen de relleno se extiende para formar un patrón. |
| Fotograma     | La imagen de relleno se convierte en un borde para la forma. |



 

*Atributo estándar de VML*

**Ejemplo**

El trazo de la forma tiene una textura en mosaico creada a partir de cylinder.gif imagen.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 