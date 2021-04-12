---
description: Indica si se debe analizar un trazo como parte de un dibujo o como parte de la escritura.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumeración StrokeType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278006"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="2a0e7-103">Enumeración StrokeType</span><span class="sxs-lookup"><span data-stu-id="2a0e7-103">StrokeType enumeration</span></span>

<span data-ttu-id="2a0e7-104">Indica si se debe analizar un trazo como parte de un dibujo o como parte de la escritura.</span><span class="sxs-lookup"><span data-stu-id="2a0e7-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a0e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a0e7-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="2a0e7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2a0e7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2a0e7-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType sin \_ clasificar**</span><span class="sxs-lookup"><span data-stu-id="2a0e7-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="2a0e7-108">El trazo puede formar parte de un dibujo o de una parte de la escritura.</span><span class="sxs-lookup"><span data-stu-id="2a0e7-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="2a0e7-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Escritura de StrokeType \_**</span><span class="sxs-lookup"><span data-stu-id="2a0e7-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="2a0e7-110">El trazo forma parte de la escritura.</span><span class="sxs-lookup"><span data-stu-id="2a0e7-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="2a0e7-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Dibujo de StrokeType \_**</span><span class="sxs-lookup"><span data-stu-id="2a0e7-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="2a0e7-112">El trazo forma parte de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="2a0e7-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2a0e7-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2a0e7-113">Examples</span></span>

<span data-ttu-id="2a0e7-114">En el ejemplo siguiente se muestra parte de un controlador de eventos de trazo, implementado de manera similar al [ejemplo de receptores de eventos de C++](c---event-sinks-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2a0e7-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="2a0e7-115">El trazo agregado se comprueba para ver si la parte superior de su cuadro de límite se ha dibujado debajo de un margen `drawingMargin` .</span><span class="sxs-lookup"><span data-stu-id="2a0e7-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="2a0e7-116">Si es así, el objeto [**IInkAnalyzer**](iinkanalyzer.md) , `m_spInkAnalyzer` , se establece para analizar el trazo como un trazo de dibujo, en lugar de como un trazo de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="2a0e7-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="2a0e7-117">`CheckHResult` es una función que toma un `HRESULT` y una cadena, y produce una excepción creada con la cadena si el `HRESULT` no es **correcto**.</span><span class="sxs-lookup"><span data-stu-id="2a0e7-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="2a0e7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a0e7-118">Requirements</span></span>



| <span data-ttu-id="2a0e7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a0e7-119">Requirement</span></span> | <span data-ttu-id="2a0e7-120">Value</span><span class="sxs-lookup"><span data-stu-id="2a0e7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0e7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a0e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0e7-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2a0e7-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2a0e7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a0e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0e7-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2a0e7-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2a0e7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a0e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a0e7-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2a0e7-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a0e7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a0e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a0e7-128">**IInkAnalyzer:: SetStrokeType (método)**</span><span class="sxs-lookup"><span data-stu-id="2a0e7-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




