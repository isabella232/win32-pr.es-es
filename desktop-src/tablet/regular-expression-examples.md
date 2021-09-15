---
description: En los ejemplos siguientes se muestran algunas expresiones regulares de escritura a mano que puede crear.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Ejemplos de expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe207be6378754bfe4b3e504d51e6ff49cadba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574453"
---
# <a name="regular-expression-examples"></a>Ejemplos de expresiones regulares

En los ejemplos siguientes se muestran algunas expresiones regulares de escritura a mano que puede crear.



| Expression                                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                               | Coincide                                                                          | No coincide                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s(!IS \_ ONECHAR)+p<br/>                                                                                                                                                                                                                                                                | Coincide con cualquier palabra que comienza con minúsculas "s", contiene uno o varios caracteres (tal y como se define en el ámbito de entrada IS ONECHAR) y termina con una \_ "p" en minúsculas.<br/> | stop<br/> sopa<br/> Arrastrar<br/> s234p<br/>               | Stop<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Coincide con cualquier dígito único, del 1 al 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Uno<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -)+<br/>                                                                                                                                                                                                                                            | Coincide con uno o varios dígitos individuales, comas o guiones. Resulta útil para limitar la entrada a un intervalo o conjunto de números, como un intervalo de páginas que se van a imprimir.<br/>               | 1<br/> 1-6<br/> 2,4,7<br/> 2-6,9,135<br/> ,,,<br/> | tres<br/> Del 7 al 9<br/>   |
| (0 \| \| 1 2 \| \| 3 4 \| \| 5 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| \| 5 \| 6 \| 7 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| \| 6 \| 7 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| \| 45 \| 6 \| 7 \| 8 \| 9)-(0 \| \| 1 2 \| \| 3 \| 4 \| 5 \| 6 7 \| 8 \| 9)(0 \| \| 1 2 \| 3 \| \| 4 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| \| 5 6 \| 7 \| 8 \| 9)<br/> | Número de la seguridad social. El formato de un número de la seguridad social *es nnn*  -  *nnn*  -  *nnnn.*<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




