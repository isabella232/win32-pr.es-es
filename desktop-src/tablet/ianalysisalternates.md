---
description: Contiene una colección de objetos que implementan la interfaz IAnalysisAlternate y que son el resultado del análisis de tinta.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interfaz IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696548"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="7a559-103">Interfaz IAnalysisAlternates</span><span class="sxs-lookup"><span data-stu-id="7a559-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="7a559-104">Contiene una colección de objetos que implementan la interfaz [**IAnalysisAlternate**](ianalysisalternate.md) y que son el resultado del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="7a559-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="7a559-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a559-105">Members</span></span>

<span data-ttu-id="7a559-106">La interfaz **IAnalysisAlternates** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7a559-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7a559-107">**IAnalysisAlternates** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7a559-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="7a559-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7a559-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7a559-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7a559-109">Methods</span></span>

<span data-ttu-id="7a559-110">La interfaz **IAnalysisAlternates** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7a559-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="7a559-111">Método</span><span class="sxs-lookup"><span data-stu-id="7a559-111">Method</span></span>                                                                   | <span data-ttu-id="7a559-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a559-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a559-113">**GetAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="7a559-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="7a559-114">Recupera el objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="7a559-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="7a559-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="7a559-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="7a559-116">Recupera el número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contenidos en la colección **IAnalysisAlternates** .</span><span class="sxs-lookup"><span data-stu-id="7a559-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a559-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a559-117">Remarks</span></span>

<span data-ttu-id="7a559-118">Esta interfaz es equivalente a la clase [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7a559-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a559-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a559-119">Requirements</span></span>



| <span data-ttu-id="7a559-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a559-120">Requirement</span></span> | <span data-ttu-id="7a559-121">Value</span><span class="sxs-lookup"><span data-stu-id="7a559-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a559-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a559-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a559-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7a559-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a559-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a559-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a559-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7a559-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7a559-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a559-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a559-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7a559-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7a559-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a559-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a559-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a559-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7a559-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a559-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a559-131">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="7a559-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="7a559-132">**IInkAnalyzer:: GetAlternates (método)**</span><span class="sxs-lookup"><span data-stu-id="7a559-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="7a559-133">**IInkAnalyzer:: GetAlternatesForContextNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="7a559-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="7a559-134">**IInkAnalyzer:: GetAlternatesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="7a559-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7a559-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7a559-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

