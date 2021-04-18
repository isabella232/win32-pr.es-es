---
description: Modifica el tipo de confirmación, que controla lo que el objeto IInkAnalyzer puede cambiar sobre IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'IContextNode:: confirm (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652436"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="eebdc-103">IContextNode:: confirm (método)</span><span class="sxs-lookup"><span data-stu-id="eebdc-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="eebdc-104">Modifica el tipo de confirmación, que controla lo que el objeto [**IInkAnalyzer**](iinkanalyzer.md) puede cambiar sobre [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="eebdc-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eebdc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eebdc-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="eebdc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eebdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebdc-107">*confirmedType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eebdc-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebdc-108">[**ConfirmationType**](confirmationtype.md) que se aplica al nodo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebdc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eebdc-109">Return value</span></span>

<span data-ttu-id="eebdc-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="eebdc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eebdc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eebdc-111">Remarks</span></span>

<span data-ttu-id="eebdc-112">Use este método para permitir que el usuario final confirme que [**IInkAnalyzer**](iinkanalyzer.md) ha analizado correctamente los trazos.</span><span class="sxs-lookup"><span data-stu-id="eebdc-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="eebdc-113">Después de llamar a **IContextNode:: CONFIRM** , **IInkAnalyzer** no cambiará los objetos [**IContextNode**](icontextnode.md) para esos trazos durante el análisis posterior.</span><span class="sxs-lookup"><span data-stu-id="eebdc-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="eebdc-114">Use **IContextNode:: CONFIRM** cuando el usuario haya confirmado los resultados del análisis y no desee que [**IInkAnalyzer**](iinkanalyzer.md) cambie un [**IContextNode**](icontextnode.md) durante el análisis posterior.</span><span class="sxs-lookup"><span data-stu-id="eebdc-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="eebdc-115">Por ejemplo, si el usuario escribe la palabra "en" y, a continuación, la aplicación llama al [**método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md), el analizador de tinta genera un nodo InkWord con el valor de "a".</span><span class="sxs-lookup"><span data-stu-id="eebdc-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="eebdc-116">Si el usuario agrega entonces "me" después de "to" como una palabra y la aplicación llama de nuevo al **método IInkAnalyzer:: Analyze** , el analizador de tinta puede quitar el nodo InkWord anterior y crear un nuevo nodo InkWord con el valor "Tomé".</span><span class="sxs-lookup"><span data-stu-id="eebdc-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="eebdc-117">Sin embargo, si después de la primera llamada al **método IInkAnalyzer:: Analyze**, la aplicación llama a **IContextNode:: CONFIRM** en el nodo InkWord de "to" con el valor [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, antes de que el usuario agregue "me", cuando la aplicación llama al **método IInkAnalyzer:: Analyze**, el analizador de tinta no quita ni cambia el nodo "to".</span><span class="sxs-lookup"><span data-stu-id="eebdc-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="eebdc-118">En su lugar, el analizador de tinta puede reconocer dos nodos InkWord para "to" y "me".</span><span class="sxs-lookup"><span data-stu-id="eebdc-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="eebdc-119">[**IContextNode**](icontextnode.md) solo puede confirmar objetos de tipo InkWord y InkDrawing (consulte [tipos de nodos de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="eebdc-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="eebdc-120">**IContextNode:: CONFIRM** devuelve **E \_ INVALIDARG** cuando el nodo no es un nodo hoja.</span><span class="sxs-lookup"><span data-stu-id="eebdc-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="eebdc-121">El [**método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md) y [**IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md) no confirman ningún nodo del que se quiten los datos de trazo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="eebdc-122">[**IContextNode:: SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)y [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) devuelven el **núcleo \_ E \_ INVALIDOPERATION** si el objeto [**IContextNode**](icontextnode.md) ya está confirmado.</span><span class="sxs-lookup"><span data-stu-id="eebdc-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="eebdc-123">[**IContextNode:: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) devuelve un error si se confirma el nodo de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="eebdc-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="eebdc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eebdc-124">Requirements</span></span>



| <span data-ttu-id="eebdc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eebdc-125">Requirement</span></span> | <span data-ttu-id="eebdc-126">Value</span><span class="sxs-lookup"><span data-stu-id="eebdc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eebdc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eebdc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eebdc-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="eebdc-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eebdc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eebdc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eebdc-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eebdc-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eebdc-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eebdc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="eebdc-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eebdc-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eebdc-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eebdc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eebdc-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eebdc-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eebdc-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="eebdc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebdc-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="eebdc-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="eebdc-137">**IContextNode::IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="eebdc-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="eebdc-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="eebdc-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




