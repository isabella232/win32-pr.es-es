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
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="1bc05-103">Propiedad Confidence \[ sobre el reconocimiento\]</span><span class="sxs-lookup"><span data-stu-id="1bc05-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="1bc05-104">Para obtener un nivel de confianza para cada resultado de reconocimiento, puede obtener la propiedad [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) del objeto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) o la propiedad [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) del objeto de [**gesto**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .</span><span class="sxs-lookup"><span data-stu-id="1bc05-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="1bc05-105">El nivel de confianza es un número que indica el grado de confianza para cada resultado de reconocimiento alternativo que el reconocedor devuelve para un segmento de reconocimiento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1bc05-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="1bc05-106">La confianza se devuelve como baja, media o alta.</span><span class="sxs-lookup"><span data-stu-id="1bc05-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="1bc05-107">La aplicación usa estos resultados para:</span><span class="sxs-lookup"><span data-stu-id="1bc05-107">The application uses these results to:</span></span>

-   <span data-ttu-id="1bc05-108">Indique al usuario que existen varias posibilidades.</span><span class="sxs-lookup"><span data-stu-id="1bc05-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="1bc05-109">Clasifique las alternativas por nivel de confianza.</span><span class="sxs-lookup"><span data-stu-id="1bc05-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="1bc05-110">Qué afecta a la confianza</span><span class="sxs-lookup"><span data-stu-id="1bc05-110">What Affects Confidence</span></span>

<span data-ttu-id="1bc05-111">Algunas de las cosas que dificultan el reconocimiento de escritura a mano y que afectan a la confianza incluyen:</span><span class="sxs-lookup"><span data-stu-id="1bc05-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="1bc05-112">Dificultad para determinar la segmentación de palabras</span><span class="sxs-lookup"><span data-stu-id="1bc05-112">Difficulty determining word segmentation</span></span>

![imagen que muestra la escritura demasiado cercana](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="1bc05-114">Dificultades en caso</span><span class="sxs-lookup"><span data-stu-id="1bc05-114">Case difficulties</span></span>

![imagen que muestra dificultades con versiones manuscritas de la palabra "Case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="1bc05-116">Estilos de escritura no comunes</span><span class="sxs-lookup"><span data-stu-id="1bc05-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="1bc05-117">Puntuación aislada</span><span class="sxs-lookup"><span data-stu-id="1bc05-117">Isolated punctuation</span></span>

![imagen que muestra comillas que están demasiado lejos del texto](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="1bc05-119">Caracteres acentuados en reconocedores en inglés</span><span class="sxs-lookup"><span data-stu-id="1bc05-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="1bc05-120">La evaluación de confianza solo está disponible para Estados Unidos inglés y para todos los reconocedores de gestos en esta versión.</span><span class="sxs-lookup"><span data-stu-id="1bc05-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="1bc05-121">Los métodos que proporcionan la propiedad Confidence para cualquier otro reconocedor devolverán **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="1bc05-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



