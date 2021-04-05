---
description: Un reconocedor puede encontrar varias maneras de dividir una muestra de entrada manuscrita en segmentos de reconocimiento. Por este motivo, el número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de tinta.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmentos de tinta y alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082095"
---
# <a name="ink-segments-and-alternates"></a><span data-ttu-id="b7b4e-104">Segmentos de tinta y alternativas</span><span class="sxs-lookup"><span data-stu-id="b7b4e-104">Ink Segments and Alternates</span></span>

<span data-ttu-id="b7b4e-105">Un reconocedor puede encontrar varias maneras de dividir una muestra de entrada manuscrita en segmentos de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="b7b4e-105">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="b7b4e-106">Por este motivo, el número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de tinta.</span><span class="sxs-lookup"><span data-stu-id="b7b4e-106">Because of this, the number of recognition alternates may be staggering, even for a small ink sample.</span></span>

<span data-ttu-id="b7b4e-107">Por ejemplo, "t o g e t h e r" puede producir los siguientes resultados:</span><span class="sxs-lookup"><span data-stu-id="b7b4e-107">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="b7b4e-108">"para obtener" (más alternativas para cada palabra)</span><span class="sxs-lookup"><span data-stu-id="b7b4e-108">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="b7b4e-109">"para recopilar" (más alternativas para cada palabra)</span><span class="sxs-lookup"><span data-stu-id="b7b4e-109">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="b7b4e-110">"TOG ether" (más alternativas para cada palabra)</span><span class="sxs-lookup"><span data-stu-id="b7b4e-110">"tog ether" (plus alternates for each word)</span></span>
-   <span data-ttu-id="b7b4e-111">"TOG" (más alternativas para cada palabra)</span><span class="sxs-lookup"><span data-stu-id="b7b4e-111">"tog at her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="b7b4e-112">"juntos" (más alternativas para la palabra)</span><span class="sxs-lookup"><span data-stu-id="b7b4e-112">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="b7b4e-113">El objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) admite el almacenamiento eficaz de los resultados de reconocimiento completo en el objeto de [**entrada manuscrita**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b4e-113">The [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object supports efficient storage of full recognition results within the [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="b7b4e-114">El objeto de **entrada manuscrita** asigna las alternativas de reconocimiento a los trazos del objeto de **entrada manuscrita** y puede contener también otra información, como la posición de línea base, los índices de línea e intervalos de idioma.</span><span class="sxs-lookup"><span data-stu-id="b7b4e-114">The **Ink** object maps the recognition alternates to the strokes in the **Ink** object and may also contain other information such as baseline position, line indices, and language ranges.</span></span>

 

 



