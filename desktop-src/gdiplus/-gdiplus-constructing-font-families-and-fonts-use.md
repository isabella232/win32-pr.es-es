---
description: Windows GDI+ agrupa las fuentes con el mismo tipo de letra pero estilos diferentes en familias de fuentes.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construir familias de fuentes y fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc405883eadd85b5b8018f75da270085197aed4792bf1c6848628cce02f457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015205"
---
# <a name="constructing-font-families-and-fonts"></a>Construir familias de fuentes y fuentes

Windows GDI+ agrupa las fuentes con el mismo tipo de letra pero estilos diferentes en familias de fuentes. Por ejemplo, la familia de fuentes de Arial contiene las fuentes siguientes:

-   Arial Regular
-   Arial Bold
-   Cursiva de Arial
-   Cursiva en negrita de Arial

GDI+ usa cuatro estilos para formar familias: normal, negrita, cursiva y cursiva en negrita. Los adjetivos como *estrechos* *y redondeados no* se consideran estilos; sino que forman parte del nombre de familia. Por ejemplo, Arial Narrow es una familia de fuentes cuyos miembros son los siguientes:

-   Arial Narrow Regular
-   Negrita estrecha de Arial
-   Cursiva estrecha de Arial
-   Cursiva en negrita estrecha de Arial

Para poder dibujar texto con GDI+, debe construir un objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) y un [**objeto Font.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Los **objetos FontFamily** especifican el tipo de letra (por ejemplo, Arial) y el objeto **Font** especifica el tamaño, el estilo y las unidades.

En el ejemplo siguiente se crea una fuente Arial de estilo normal con un tamaño de 16 píxeles:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



En el código anterior, el primer argumento pasado al constructor [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) es la dirección del [**objeto FontFamily.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) El segundo argumento especifica el tamaño de la fuente medida en unidades identificadas por el cuarto argumento. El tercer argumento identifica el estilo.

[*:UnitPixel**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) es miembro de la enumeración **Unit** y [*:FontStyleModer**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) es miembro de la **enumeración FontStyle.** Ambas enumeraciones se declaran en Gdiplusenums.h.

 

 



