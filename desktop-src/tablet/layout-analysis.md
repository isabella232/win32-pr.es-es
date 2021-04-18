---
description: El análisis de diseño funciona en una colección de trazos y clasifica los trazos en elementos de escritura a mano y de dibujo. El objeto divisor proporciona acceso a las características de análisis del diseño de Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Análisis de diseño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720568"
---
# <a name="layout-analysis"></a><span data-ttu-id="5fcd9-104">Análisis de diseño</span><span class="sxs-lookup"><span data-stu-id="5fcd9-104">Layout Analysis</span></span>

<span data-ttu-id="5fcd9-105">El análisis de diseño funciona en una colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) y clasifica los trazos en elementos de escritura a mano y de dibujo.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="5fcd9-106">El objeto [**divisor**](inkdivider-class.md) proporciona acceso a las características de análisis del diseño de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="5fcd9-107">En la tabla siguiente se describen los tipos de elementos estructurales de la enumeración [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) en la que el objeto [**divisor**](inkdivider-class.md) clasifica los trazos.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="5fcd9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fcd9-108">Type</span></span>          | <span data-ttu-id="5fcd9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fcd9-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fcd9-110">**Segmento**</span><span class="sxs-lookup"><span data-stu-id="5fcd9-110">**Segment**</span></span>   | <span data-ttu-id="5fcd9-111">Un segmento de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="5fcd9-112">**Line**</span><span class="sxs-lookup"><span data-stu-id="5fcd9-112">**Line**</span></span>      | <span data-ttu-id="5fcd9-113">Línea de escritura a mano que contiene uno o más segmentos de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="5fcd9-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="5fcd9-114">**Paragraph**</span></span> | <span data-ttu-id="5fcd9-115">Bloque de trazos que contiene una o más líneas de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="5fcd9-116">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="5fcd9-116">**Drawing**</span></span>   | <span data-ttu-id="5fcd9-117">Tinta que no es de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="5fcd9-118">El objeto [**divisor**](inkdivider-class.md) tiene una colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , que el objeto **divisor** analiza dinámicamente cada vez que se agrega o se elimina de la colección.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="5fcd9-119">El objeto **divisor** no es Serializable y no se puede guardar su estado de análisis.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="5fcd9-120">Por lo tanto, el objeto **divisor** está diseñado para las aplicaciones que deben diferenciar entre escritura a mano mixta y entrada de dibujo, pero no es necesario volver a analizar grandes cantidades de tinta entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="5fcd9-121">Puede obtener una instantánea estática del resultado del análisis actual, que se devuelve en un objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="5fcd9-122">Puede obtener objetos [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , cada uno de los cuales representa un único elemento estructural de un objeto **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="5fcd9-123">Los objetos **DivisionResult** y **DivisionUnit** no son serializables.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="5fcd9-124">Sin embargo, la información de estado de estos objetos está disponible.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="5fcd9-125">El objeto [**divisor**](inkdivider-class.md) funciona solo con escritura a mano de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="5fcd9-126">Para que el objeto **divisor** analice los idiomas verticales como el chino correctamente, los caracteres deben dibujarse de izquierda a derecha en lugar de arriba a abajo.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

