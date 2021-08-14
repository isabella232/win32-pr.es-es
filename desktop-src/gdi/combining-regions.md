---
description: Una aplicación combina dos regiones mediante una llamada a la función CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinar regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6550f260a70bc0f49e6b181f9e1c82a64ce4eadbe643214362444d0dcbfccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887525"
---
# <a name="combining-regions"></a>Combinar regiones

Una aplicación combina dos regiones mediante una llamada a la [**función CombineRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) Con esta función, una aplicación puede combinar las partes en intersección de dos regiones, todas menos las partes que se intersecan de dos regiones, las dos regiones originales en su totalidad, y así sucesivamente. A continuación se encuentran cinco valores que definen las combinaciones de regiones.



| Valor     | Significado                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ Y  | Las partes en intersección de dos regiones originales definen una nueva región.                   |
| RGN \_ COPY | Una copia de la primera (de las dos regiones originales) define una nueva región.               |
| DIFERENCIA DE \_ RGN | La parte de la primera región que no forma intersección con la segunda define una nueva región. |
| RGN \_ O   | Las dos regiones originales definen una nueva región.                                         |
| RGN \_ XOR  | Las partes de las dos regiones originales que no se superponen definen una nueva región.      |



 

En la ilustración siguiente se muestran las cinco combinaciones posibles de un cuadrado y una región circular resultantes de una llamada a [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).

![ilustración que muestra los resultados descritos en la tabla anterior](images/csrgn-02.png)

 

 



