---
description: Para obtener un nivel de confianza para cada resultado de reconocimiento, puede obtener la propiedad Confidence del objeto RecognitionAlternate o la propiedad Confidence del objeto Gesture.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Propiedad Confidence [Acerca del reconocimiento]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466278"
---
# <a name="confidence-property-about-recognition"></a>Propiedad De confianza \[ sobre el reconocimiento\]

Para obtener un nivel de confianza para cada resultado de reconocimiento, puede obtener la propiedad [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) del objeto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) o la propiedad [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) del [**objeto Gesture.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) El nivel de confianza es un número que indica el grado de confianza para cada resultado de reconocimiento alternativo que el reconocedor devuelve para un segmento de reconocimiento correspondiente.

La confianza se devuelve como baja, media o alta. La aplicación usa estos resultados para:

-   Indique al usuario que existen varias posibilidades.
-   Clasifice las alternativas por nivel de confianza.

## <a name="what-affects-confidence"></a>Qué afecta a la confianza

Algunas de las cosas que dificultan el reconocimiento de escritura a mano y afectan a la confianza son:

-   Dificultad para determinar la segmentación de palabras

![imagen en la que se muestra la escritura demasiado cercana](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Dificultades de los casos

![imagen que muestra dificultades con las versiones manuscritas de la palabra "case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Estilos de escritura poco comunes
-   Puntuación aislada

![imagen que muestra comillas que están demasiado lejos del texto](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Caracteres acentuados en reconocedores en inglés

> [!Note]  
> La evaluación de confianza solo está disponible para Estados Unidos inglés y todos los reconocedores de gestos de esta versión. Los métodos que proporcionan la propiedad de confianza para cualquier otro reconocedor **devolverán E \_ NOTIMPL**.

 

 

 



