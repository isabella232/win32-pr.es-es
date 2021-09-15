---
description: Los reconocedores de texto dividen una muestra de lápiz en segmentos y traducen los segmentos de entrada de lápiz en texto.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Reconocedores de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372af61d45bb1cc8bcd8377202149073c3decc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467951"
---
# <a name="text-recognizers"></a>Reconocedores de texto

Los reconocedores de texto dividen una muestra de lápiz en segmentos y traducen los segmentos de entrada de lápiz en texto. Esto es útil para reconocer la escritura a mano. También es útil en escenarios de escritura complejos, como reconocer glifos kanji individuales y ofrecer a los usuarios la finalización automática de un carácter mientras lo escriben.

Un reconocedor de texto devuelve una cadena Unicode para cada segmento de reconocimiento de entrada de lápiz. La cadena que acompaña es el nivel de confianza que el reconocedor asigna al resultado y una asignación del resultado a la entrada de lápiz original. Esta asignación muestra qué segmento de la entrada de lápiz original corresponde a la cadena de código Unicode. La cadena que representa la salida del reconocedor de texto siempre se representa en el orden lineal, en lugar del orden espacial o cronológico en el que se han especificado los segmentos.

En la tabla siguiente se enumeran los idiomas admitidos por los reconocedores de escritura a mano de Microsoft y las versiones Windows en las que se introdujeron por primera vez estos idiomas. Tenga en cuenta que es posible que algunos reconocedores de idioma no estén disponibles en determinadas versiones de Windows y que deban descargarse por separado. Los reconocedores de terceros también pueden estar disponibles para idiomas adicionales, pero no necesariamente aprobados por Microsoft.



| Idioma                                   | Windows XP Tablet PC Edition | Windows XP Tablet PC Edition 2005 | Windows Vista | Windows 7 |
|--------------------------------------------|------------------------------|-----------------------------------|---------------|-----------|
| Chino (simplificado y tradicional)       | X                            |                                   |               |           |
| Inglés (EE. UU., Reino Unido, Canadá y Australia)    | X                            |                                   |               |           |
| Francés                                     | X                            |                                   |               |           |
| Alemán                                     | X                            |                                   |               |           |
| Japonés                                   | X                            |                                   |               |           |
| Coreano                                     | X                            |                                   |               |           |
| Español                                    | X                            |                                   |               |           |
| Italiano                                    |                              | X                                 |               |           |
| Neerlandés (Países Bajos y Bélgica)            |                              |                                   | X             |           |
| Portugués (Brasil y portugués/neutro) |                              |                                   | X             |           |
| Catalán                                    |                              |                                   |               | X         |
| Croata                                   |                              |                                   |               | X         |
| Checo                                      |                              |                                   |               | X         |
| Danés                                     |                              |                                   |               | X         |
| Finés                                    |                              |                                   |               | X         |
| Alemán (Suiza)                       |                              |                                   |               | X         |
| Noruego (Bokmal y Nyno norwegian)             |                              |                                   |               | X         |
| Polaco                                     |                              |                                   |               | X         |
| Portugués (Portugal)                      |                              |                                   |               | X         |
| Rumano                                   |                              |                                   |               | X         |
| Ruso                                    |                              |                                   |               | X         |
| Serbio (cirílico y latino)               |                              |                                   |               | X         |
| Español (Argentina y México)             |                              |                                   |               | X         |
| Sueco                                    |                              |                                   |               | X         |



 

 

 



