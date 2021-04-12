---
description: 'Tenga en cuenta lo siguiente al decidir cuándo y cómo usar el objeto divisor en una aplicación:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Otras consideraciones del divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277780"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="8bd1e-103">Otras consideraciones del divisor</span><span class="sxs-lookup"><span data-stu-id="8bd1e-103">Other Divider Considerations</span></span>

<span data-ttu-id="8bd1e-104">Tenga en cuenta lo siguiente al decidir cuándo y cómo usar el objeto [**divisor**](inkdivider-class.md) en una aplicación:</span><span class="sxs-lookup"><span data-stu-id="8bd1e-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="8bd1e-105">El objeto [**divisor**](inkdivider-class.md) está diseñado para separar dibujos y bloques de escritura a mano, pero no para reconocer niveles más altos de estructura, como tablas o columnas.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="8bd1e-106">El objeto [**divisor**](inkdivider-class.md) no proporciona interfaces específicamente para la corrección de los resultados del análisis de diseño.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="8bd1e-107">El uso del tiempo de espera y el número de heurísticas de trazo para agregar o quitar varios trazos a la vez desde los trazos del objeto de [**divisor**](inkdivider-class.md) pueden mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="8bd1e-108">Consideraciones de análisis</span><span class="sxs-lookup"><span data-stu-id="8bd1e-108">Reanalysis Considerations</span></span>

<span data-ttu-id="8bd1e-109">Si está pensando en utilizar el objeto [**divisor**](inkdivider-class.md) en una aplicación en la que el objeto **divisor** puede tener que volver a analizar grandes cantidades de tinta, tenga en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="8bd1e-110">Conservar copias de lápiz y trazos</span><span class="sxs-lookup"><span data-stu-id="8bd1e-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="8bd1e-111">Una aplicación puede mantener copias de los objetos [**Ink**](inkdisp-class.md) y [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) de los elementos de la aplicación que se pueden revisar posteriormente en la sesión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="8bd1e-112">Esto elimina la necesidad de volver a analizar el objeto de **entrada manuscrita** si el usuario vuelve al elemento.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="8bd1e-113">Este enfoque se desaconseja de la memoria para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="8bd1e-114">Heurística de reducción de datos</span><span class="sxs-lookup"><span data-stu-id="8bd1e-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="8bd1e-115">Es posible que pueda grabar los resultados del análisis como datos de la aplicación e implementar la heurística para determinar cuándo se debe volver a analizar un conjunto de trazos.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="8bd1e-116">Esta práctica reduciría la necesidad de volver a analizar toda la tinta de la aplicación entre sesiones de aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="8bd1e-117">Sin embargo, se debe tener cuidado para conservar los límites de los elementos estructurales o para volver a analizar todos los trazos de los elementos afectados.</span><span class="sxs-lookup"><span data-stu-id="8bd1e-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bd1e-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bd1e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd1e-119">**Clase InkDivider**</span><span class="sxs-lookup"><span data-stu-id="8bd1e-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="8bd1e-120">[Clase Microsoft. Ink. divisor](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="8bd1e-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 
