---
description: Los reconocedores de texto dividen un ejemplo de entrada de lápiz en segmentos y traducen los segmentos de tinta en texto.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Reconocedores de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372af61d45bb1cc8bcd8377202149073c3decc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817707"
---
# <a name="text-recognizers"></a>Reconocedores de texto

Los reconocedores de texto dividen un ejemplo de entrada de lápiz en segmentos y traducen los segmentos de tinta en texto. Esto resulta útil para reconocer la escritura a mano. También es útil en escenarios de escritura complejos, como reconocer glifos kanji individuales y ofrecer a los usuarios la finalización automática de un carácter mientras lo escriben.

Un reconocedor de texto devuelve una cadena Unicode para cada segmento de reconocimiento de tinta. La cadena adjunta es el nivel de confianza que el reconocedor asigna al resultado y una asignación del resultado a la tinta original. Esta asignación muestra qué segmento de la tinta original corresponde a la cadena de código Unicode. La cadena que representa la salida del reconocedor de texto siempre se representa en el orden lineal, en lugar de en el orden espacial o en el orden cronológico en el que se han introducido los segmentos.

En la tabla siguiente se enumeran los idiomas admitidos por los reconocedores de escritura a mano de Microsoft y las versiones de Windows en las que se introdujeron por primera vez estos lenguajes. Tenga en cuenta que es posible que algunos reconocedores de idioma no estén disponibles en determinada versión de Windows y que se deban descargar por separado. Los reconocedores de terceros también pueden estar disponibles para idiomas adicionales, pero Microsoft no los ha aprobado necesariamente.



| Idioma                                   | Windows XP Tablet PC Edition | Windows XP Tablet PC Edition 2005 | Windows Vista | Windows 7 |
|--------------------------------------------|------------------------------|-----------------------------------|---------------|-----------|
| Chino (simplificado y tradicional)       | X                            |                                   |               |           |
| Inglés (EE. UU., Reino Unido, Canadá y Australia)    | X                            |                                   |               |           |
| Francés                                     | X                            |                                   |               |           |
| Alemán                                     | X                            |                                   |               |           |
| Japonés                                   | X                            |                                   |               |           |
| Coreano                                     | X                            |                                   |               |           |
| Español                                    | X                            |                                   |               |           |
| Italiano                                    |                              | X                                 |               |           |
| Holandés (Países Bajos y Bélgica)            |                              |                                   | X             |           |
| Portugués (Brasil y Portugués/neutro) |                              |                                   | X             |           |
| Catalán                                    |                              |                                   |               | X         |
| Croata                                   |                              |                                   |               | X         |
| Checo                                      |                              |                                   |               | X         |
| Danés                                     |                              |                                   |               | X         |
| Finés                                    |                              |                                   |               | X         |
| Alemán (Suiza)                       |                              |                                   |               | X         |
| Noruego (Bokmal y Nynorsk)             |                              |                                   |               | X         |
| Polaco                                     |                              |                                   |               | X         |
| Portugués (Portugal)                      |                              |                                   |               | X         |
| Rumano                                   |                              |                                   |               | X         |
| Ruso                                    |                              |                                   |               | X         |
| Serbio (cirílico y latín)               |                              |                                   |               | X         |
| Español (Argentina y México)             |                              |                                   |               | X         |
| Sueco                                    |                              |                                   |               | X         |



 

 

 



