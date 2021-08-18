---
description: GRUPOS \_ DE CONFIGURACIÓN REGIONAL
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476fa80a22e55791ca7b5636237540c457480ff0bd9c808b99ef3c6e46a17dce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106215"
---
# <a name="locale_sgrouping"></a>GRUPOS \_ DE CONFIGURACIÓN REGIONAL

Tamaños de cada grupo de dígitos a la izquierda del decimal. El número máximo de caracteres permitido para esta cadena es de diez, incluido un carácter nulo de terminación. Se necesita un tamaño explícito para cada grupo y los tamaños se separan por punto y coma. Si el último valor es 0, se repite el valor anterior. Por ejemplo, para agrupar miles, especifique 3;0. Las configuraciones regionales indic agrupan los primeros miles y, a continuación, agrupan por cientos. Por ejemplo, 12 34 56 789 está representado por 3;2;0.

Ejemplos adicionales:



| Especificación | Cadena resultante   |
|---------------|--------------------|
| 3;0           | 3,000,000,000,000  |
| 3;2;0         | 30,00,00,00,00,000 |
| 3             | 3000000000,000     |
| 3;2           | 30000000,00,000    |



 

 

 



