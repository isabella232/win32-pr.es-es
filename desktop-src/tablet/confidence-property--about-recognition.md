---
description: Para obtener un nivel de confianza para cada resultado de reconocimiento, puede obtener la propiedad Confidence del objeto RecognitionAlternate o la propiedad Confidence del objeto de gesto.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Propiedad Confidence [acerca del reconocimiento]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907624"
---
# <a name="confidence-property-about-recognition"></a>Propiedad Confidence \[ sobre el reconocimiento\]

Para obtener un nivel de confianza para cada resultado de reconocimiento, puede obtener la propiedad [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) del objeto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) o la propiedad [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) del objeto de [**gesto**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) . El nivel de confianza es un número que indica el grado de confianza para cada resultado de reconocimiento alternativo que el reconocedor devuelve para un segmento de reconocimiento correspondiente.

La confianza se devuelve como baja, media o alta. La aplicación usa estos resultados para:

-   Indique al usuario que existen varias posibilidades.
-   Clasifique las alternativas por nivel de confianza.

## <a name="what-affects-confidence"></a>Qué afecta a la confianza

Algunas de las cosas que dificultan el reconocimiento de escritura a mano y que afectan a la confianza incluyen:

-   Dificultad para determinar la segmentación de palabras

![imagen que muestra la escritura demasiado cercana](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Dificultades en caso

![imagen que muestra dificultades con versiones manuscritas de la palabra "Case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Estilos de escritura no comunes
-   Puntuación aislada

![imagen que muestra comillas que están demasiado lejos del texto](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Caracteres acentuados en reconocedores en inglés

> [!Note]  
> La evaluación de confianza solo está disponible para Estados Unidos inglés y para todos los reconocedores de gestos en esta versión. Los métodos que proporcionan la propiedad Confidence para cualquier otro reconocedor devolverán **E \_ NOTIMPL**.

 

 

 



