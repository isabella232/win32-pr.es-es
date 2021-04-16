---
description: Especifica la guía o el área donde se dibuja y reconoce la entrada de lápiz.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Estructura InkAnalysisRecognizerGuide (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696338"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="f0ac7-103">Estructura InkAnalysisRecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="f0ac7-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="f0ac7-104">Especifica la guía o el área donde se dibuja y reconoce la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ac7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0ac7-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="f0ac7-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0ac7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0ac7-107">**rectWritingBox**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="f0ac7-108">Área de escritura invisible de la guía de reconocimiento en la que realmente se puede realizar la escritura.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="f0ac7-109">**rectDrawnBox**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="f0ac7-110">Rectángulo que se dibuja en la pantalla de Tablet PC y en el que tiene lugar la escritura.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="f0ac7-111">**cRows**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="f0ac7-112">El número de filas en el cuadro guía de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="f0ac7-113">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="f0ac7-114">El número de columnas en el cuadro guía de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="f0ac7-115">**Elips**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="f0ac7-116">El alto de la media en el cuadro de la guía de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="f0ac7-117">El alto de línea media es la distancia desde la línea de base hasta la línea media del cuadro dibujado.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0ac7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0ac7-118">Remarks</span></span>

<span data-ttu-id="f0ac7-119">Un **InkAnalysisRecognizerGuide** define un área esperada de entrada, como una línea o cuadros, para los caracteres.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="f0ac7-120">Una estructura **InkAnalysisRecognizerGuide** solo se puede establecer en un nodo de contexto de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="f0ac7-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="f0ac7-121">[**IInkAnalyzer**](iinkanalyzer.md) usa la ubicación del nodo de sugerencia de análisis y las ubicaciones de los trazos de entrada de lápiz para asociar un trazo al nodo de sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="f0ac7-122">Los trazos con una asociación al nodo de sugerencia de análisis tendrán el **InkAnalysisRecognizerGuide** especificado que se usará cuando lo reconozca un **IInkAnalyzer**, siempre que el **IInkAnalyzer** admita **InkAnalysisRecognizerGuide**.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="f0ac7-123">Los valores expresados en la clase **InkAnalysisRecognizerGuide** siempre se relacionan con la ubicación del nodo de sugerencia de análisis y se especifican en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="f0ac7-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ac7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0ac7-124">Requirements</span></span>



| <span data-ttu-id="f0ac7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ac7-125">Requirement</span></span> | <span data-ttu-id="f0ac7-126">Value</span><span class="sxs-lookup"><span data-stu-id="f0ac7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ac7-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0ac7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ac7-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f0ac7-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0ac7-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0ac7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ac7-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0ac7-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f0ac7-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0ac7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ac7-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ac7-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ac7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0ac7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ac7-134">Propiedades de la sugerencia de análisis</span><span class="sxs-lookup"><span data-stu-id="f0ac7-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="f0ac7-135">**IInkAnalyzer:: CreateAnalysisHint (método)**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="f0ac7-136">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0ac7-137">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f0ac7-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0ac7-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="f0ac7-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




