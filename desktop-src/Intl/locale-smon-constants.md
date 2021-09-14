---
description: Constantes \_ de SMON de LOCALE \*
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: LOCALE_SMON* Constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274332"
---
# <a name="locale_smon-constants"></a>Constantes \_ de SMON de LOCALE \*

En este tema se definen las constantes SMON de LOCALE usadas por \_ \* NLS en la representación de valores monetarios.



| Value                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LOCALE \_ SMONDECIMALSEP  | Caracteres usados como separador decimal monetario. El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación. Por ejemplo, si se muestra un importe monetario como "$3,40", del mismo modo que se muestran "tres dólares y cincuenta céntimos" en el Estados Unidos, el separador decimal monetario es ".".                                                                                                                                             |
| LOCALE \_ SMONGROUPING    | Tamaños de cada grupo de dígitos monetarios a la izquierda del decimal. El número máximo de caracteres permitido para esta cadena es de diez, incluido un carácter nulo de terminación. Se necesita un tamaño explícito para cada grupo y los tamaños se separan por punto y coma. Si el último valor es 0, se repite el valor anterior. Por ejemplo, para agrupar miles, especifique 3;0. Los idiomas indic agrupan los primeros miles y, a continuación, agrupan por cientos. Por ejemplo, 12 34 56 789 se representa mediante 3;2;0. |
| LOCALE \_ SMONTHOUSANDSEP | Caracteres usados como separador monetario entre grupos de dígitos a la izquierda del decimal. El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación. Normalmente, los grupos representan miles. Sin embargo, dependiendo del valor especificado para LOCALE \_ SMONGROUPING, pueden representar otra cosa.                                                                                                                                 |



 

 

 



