---
description: Windows GDI+ agrupa fuentes con el mismo tipo de letra pero con distintos estilos en familias de fuentes.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construir fuentes y familias de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997516"
---
# <a name="constructing-font-families-and-fonts"></a>Construir fuentes y familias de fuentes

Windows GDI+ agrupa fuentes con el mismo tipo de letra pero con distintos estilos en familias de fuentes. Por ejemplo, la familia de fuentes Arial contiene las siguientes fuentes:

-   Arial normal
-   Arial negrita
-   Arial cursiva
-   Arial negrita cursiva

GDI+ utiliza cuatro estilos para formar familias: normal, negrita, cursiva y negrita cursiva. Los adjetivos como *estrechos* y *redondeados* no se consideran estilos; en su lugar, forman parte del nombre de familia. Por ejemplo, Arial Narrow es una familia de fuentes cuyos miembros son los siguientes:

-   Arial Narrow regular
-   Arial Narrow negrita
-   Arial Narrow cursiva
-   Arial Narrow negrita cursiva

Antes de poder dibujar texto con GDI+, debe construir un objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) y un objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Los objetos **FontFamily** especifican el tipo de letra (por ejemplo, Arial) y el objeto **Font** especifica el tamaño, el estilo y las unidades.

En el ejemplo siguiente se crea una fuente Arial de estilo normal con un tamaño de 16 píxeles:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



En el código anterior, el primer argumento pasado al constructor de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) es la dirección del objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . El segundo argumento especifica el tamaño de la fuente que se mide en unidades identificadas por el cuarto argumento. El tercer argumento identifica el estilo.

[* * * * UnitPixel * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) * * es un miembro de la enumeración **Unit** y [* * * * FontStyleRegular * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) * * es un miembro de la enumeración **fontStyle** . Ambas enumeraciones se declaran en Gdiplusenums. h.

 

 



