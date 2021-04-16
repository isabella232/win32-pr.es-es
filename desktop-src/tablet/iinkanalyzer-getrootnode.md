---
description: Obtiene el IContextNode raíz del árbol de contexto del objeto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'IInkAnalyzer:: GetRootNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696522"
---
# <a name="iinkanalyzergetrootnode-method"></a><span data-ttu-id="c828b-103">IInkAnalyzer:: GetRootNode (método)</span><span class="sxs-lookup"><span data-stu-id="c828b-103">IInkAnalyzer::GetRootNode method</span></span>

<span data-ttu-id="c828b-104">Obtiene el [**IContextNode**](icontextnode.md) raíz del árbol de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="c828b-104">Gets the root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="c828b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c828b-105">Syntax</span></span>


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a><span data-ttu-id="c828b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c828b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c828b-107">*ppRootNode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c828b-107">*ppRootNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c828b-108">[**IContextNode**](icontextnode.md) raíz del árbol de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="c828b-108">The root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c828b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c828b-109">Return value</span></span>

<span data-ttu-id="c828b-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c828b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c828b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c828b-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c828b-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppRootNode* cuando ya no necesite usar el nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="c828b-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppRootNode* when you no longer need to use the root node.</span></span>

 

<span data-ttu-id="c828b-113">[**IInkAnalyzer**](iinkanalyzer.md) mantiene un árbol de objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c828b-113">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a tree of [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="c828b-114">Estos objetos contienen la entrada para el análisis y los resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="c828b-114">These objects contain both input for analysis and the results of analysis.</span></span> <span data-ttu-id="c828b-115">Cuando los trazos se agregan inicialmente al **IInkAnalyzer**, el **IInkAnalyzer** los asigna a un **IContextNode** de tipo UnclassifiedInk (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y tipos de nodo de [contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="c828b-115">When strokes are initially added to the **IInkAnalyzer**, the **IInkAnalyzer** assigns them to a **IContextNode** of type UnclassifiedInk (See [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="c828b-116">Una vez analizados los trazos, el **IInkAnalyzer** los asigna a los objetos **IContextNode** adecuados en el árbol.</span><span class="sxs-lookup"><span data-stu-id="c828b-116">After the strokes are analyzed, the **IInkAnalyzer** assigns them to appropriate **IContextNode** objects in the tree.</span></span> <span data-ttu-id="c828b-117">Para obtener más información sobre el uso de **IInkAnalyzer** para analizar la entrada de lápiz, consulte [información general del análisis de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c828b-117">For more information about using the **IInkAnalyzer** to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c828b-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c828b-118">Examples</span></span>

<span data-ttu-id="c828b-119">En el ejemplo siguiente se muestra un método que recorre el árbol de resultados [**IContextNode**](icontextnode.md) del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="c828b-119">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="c828b-120">Si el IInkAnlyzer no está realizando actualmente el análisis de tinta, el método hace lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c828b-120">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="c828b-121">Obtiene la cadena de reconocimiento superior.</span><span class="sxs-lookup"><span data-stu-id="c828b-121">Gets the top recognition string.</span></span>
-   <span data-ttu-id="c828b-122">Obtiene el nodo raíz del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="c828b-122">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="c828b-123">Llama a un método auxiliar, `ExploreContextNode` , para examinar el nodo raíz y sus nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c828b-123">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c828b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c828b-124">Requirements</span></span>



| <span data-ttu-id="c828b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c828b-125">Requirement</span></span> | <span data-ttu-id="c828b-126">Value</span><span class="sxs-lookup"><span data-stu-id="c828b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c828b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c828b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c828b-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c828b-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c828b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c828b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c828b-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c828b-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c828b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c828b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c828b-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c828b-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c828b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c828b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c828b-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c828b-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c828b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c828b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c828b-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c828b-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c828b-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c828b-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c828b-138">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="c828b-138">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="c828b-139">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c828b-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

