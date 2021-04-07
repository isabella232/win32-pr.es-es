---
description: configuración regional \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003221"
---
# <a name="locale_sgrouping"></a>configuración regional \_ SGROUPING

Tamaños de cada grupo de dígitos a la izquierda del separador decimal. El número máximo de caracteres permitido para esta cadena es diez, incluido un carácter nulo de terminación. Se necesita un tamaño explícito para cada grupo y los tamaños se separan mediante signos de punto y coma. Si el último valor es 0, el valor anterior se repite. Por ejemplo, para agrupar miles, especifique 3; 0. Configuraciones regionales indias agrupe los primeros mil y, después, agrupe por cientos. Por ejemplo, 12, 34, 56789 se representa mediante 3; 2; 0.

Otros ejemplos:



| Especificación | Cadena resultante   |
|---------------|--------------------|
| 3; 0           | 3 billones  |
| 3; 2; 0         | 30, 00, 00, 00, 00000 |
| 3             | 3 billones     |
| 3; 2           | 30000000, 00000    |



 

 

 



