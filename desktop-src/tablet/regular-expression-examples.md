---
description: En los ejemplos siguientes se muestran algunas expresiones regulares de escritura a mano que puede crear.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Ejemplos de expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe207be6378754bfe4b3e504d51e6ff49cadba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716903"
---
# <a name="regular-expression-examples"></a>Ejemplos de expresiones regulares

En los ejemplos siguientes se muestran algunas expresiones regulares de escritura a mano que puede crear.



| Expression                                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                               | Coincide                                                                          | No coincide                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s (! IS \_ ONECHAR) + p<br/>                                                                                                                                                                                                                                                                | Coincide con cualquier palabra que comience por "s" en minúsculas, contiene uno o más caracteres (tal y como se define en el \_ ámbito de entrada ONECHAR) y termina con una "p" minúscula.<br/> | stop<br/> sopa<br/> schlep<br/> s234p<br/>               | Stop<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Coincide con cualquier dígito individual, de 1 a 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Uno<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -) +<br/>                                                                                                                                                                                                                                            | Coincide con uno o varios dígitos, comas o guiones. Resulta útil para limitar la entrada a un intervalo o un conjunto de números, como un intervalo de páginas que se van a imprimir.<br/>               | 1<br/> 1-6<br/> 2, 4, 7<br/> 2-6, 9135<br/> ,,,<br/> | tres<br/> de 7 a 9<br/>   |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/> | Un número de la seguridad social. El formato de un número de la seguridad social es *nnn*  -  *nn*  -  *nnnn*.<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




