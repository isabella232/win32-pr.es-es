---
title: Respuesta del lector a las características de ASF
description: Respuesta del lector a las características de ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- SDK de Windows Media Format, respuestas de lector a las características de ASF
- Advanced Systems Format (ASF), respuestas de lector a características
- ASF (formato de sistemas avanzados), respuestas de lector a características
- respuestas de lector a las características de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704649"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="7692d-107">Respuesta del lector a las características de ASF</span><span class="sxs-lookup"><span data-stu-id="7692d-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="7692d-108">La mayoría de las características especiales de archivos ASF se pueden establecer en archivos para interactuar con las aplicaciones de reproducción personalizadas diseñadas para controlarlas.</span><span class="sxs-lookup"><span data-stu-id="7692d-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="7692d-109">Sin embargo, algunas de las características tienen compatibilidad integrada en el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="7692d-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="7692d-110">El objeto lector seleccionará automáticamente las secuencias de los conjuntos que se excluyen mutuamente por la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="7692d-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="7692d-111">Este caso especial se conoce como velocidad de bits múltiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="7692d-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="7692d-112">La secuencia que el lector selecciona se basa en la velocidad de bits de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7692d-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="7692d-113">El número de secuencia y el orden en el que se agregó al objeto de exclusión mutua son irrelevantes para la selección automática.</span><span class="sxs-lookup"><span data-stu-id="7692d-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="7692d-114">Si un archivo incluye más de un conjunto de flujos mutuamente excluyentes según la velocidad de bits, el lector seleccionará las secuencias basadas en el cálculo del mejor uso del ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="7692d-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="7692d-115">La exclusión mutua basada en el lenguaje se establece mediante una configuración de salida, antes de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7692d-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="7692d-116">Si combina la exclusión mutua basada en el idioma y en la velocidad de bits, debe agrupar los flujos mutuamente exclusivos basados en la velocidad de bits por lenguaje y, a continuación, hacer que los grupos sean mutuamente excluyentes por el lenguaje.</span><span class="sxs-lookup"><span data-stu-id="7692d-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="7692d-117">El lector comprobará primero el idioma y, a continuación, determinará la velocidad de bits que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7692d-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="7692d-118">La priorización de flujo se establece mediante una matriz de registros.</span><span class="sxs-lookup"><span data-stu-id="7692d-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="7692d-119">Los registros de la matriz están en orden descendente de prioridad.</span><span class="sxs-lookup"><span data-stu-id="7692d-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="7692d-120">El último flujo de la matriz es el primero que se quitará por el lector.</span><span class="sxs-lookup"><span data-stu-id="7692d-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7692d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7692d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7692d-122">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="7692d-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="7692d-123">**Exclusión mutua**</span><span class="sxs-lookup"><span data-stu-id="7692d-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="7692d-124">**Priorización de flujos**</span><span class="sxs-lookup"><span data-stu-id="7692d-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




