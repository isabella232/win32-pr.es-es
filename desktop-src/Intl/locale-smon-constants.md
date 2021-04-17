---
description: Constantes de SMON de configuración regional \_ \*
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Constantes de LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666809"
---
# <a name="locale_smon-constants"></a>Constantes de SMON de configuración regional \_ \*

En este tema se definen las \_ constantes de SMON de configuración regional \* utilizadas por NLS en que representan valores monetarios.



| Value                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| configuración regional \_ SMONDECIMALSEP  | Caracteres usados como separador decimal monetario. El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación. Por ejemplo, si se muestra un importe monetario como "$3,40", del mismo modo que se muestra "tres dólares y 40 céntimos" en el Estados Unidos, el separador decimal monetario es ".".                                                                                                                                             |
| configuración regional \_ SMONGROUPING    | Tamaños de cada grupo de dígitos monetarios a la izquierda del separador decimal. El número máximo de caracteres permitido para esta cadena es diez, incluido un carácter nulo de terminación. Se necesita un tamaño explícito para cada grupo y los tamaños se separan mediante signos de punto y coma. Si el último valor es 0, el valor anterior se repite. Por ejemplo, para agrupar miles, especifique 3; 0. Los idiomas indios agrupan los primeros mil y luego agrupan por cientos. Por ejemplo, 12, 34, 56789 se representa mediante 3; 2; 0. |
| configuración regional \_ SMONTHOUSANDSEP | Caracteres usados como separador monetario entre grupos de dígitos a la izquierda del separador decimal. El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación. Normalmente, los grupos representan miles. Sin embargo, en función del valor especificado para SMONGROUPING de configuración regional \_ , pueden representar otra cosa.                                                                                                                                 |



 

 

 



