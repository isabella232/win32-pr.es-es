---
description: Una aplicación combina dos regiones mediante una llamada a la función CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinar regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556964"
---
# <a name="combining-regions"></a>Combinar regiones

Una aplicación combina dos regiones mediante una llamada a la función [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) . Mediante esta función, una aplicación puede combinar las partes de intersección de dos regiones, excepto las partes que interseccionan de dos regiones, las dos regiones originales en su totalidad, etc. A continuación se muestran cinco valores que definen las combinaciones de regiones.



| Value     | Significado                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ y  | Las partes de intersección de dos regiones originales definen una nueva región.                   |
| copia de RGN \_ | Una copia de la primera (de las dos regiones originales) define una nueva región.               |
| RGN ( \_ diferencia) | La parte de la primera región que no forma una intersección con la segunda define una nueva región. |
| RGN \_ o   | Las dos regiones originales definen una nueva región.                                         |
| RGN \_ XOR  | Las partes de las dos regiones originales que no se superponen definen una nueva región.      |



 

En la ilustración siguiente se muestran las cinco combinaciones posibles de un cuadrado y una región circular resultante de una llamada a [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).

![Ilustración en la que se muestran los resultados descritos en la tabla anterior](images/csrgn-02.png)

 

 



