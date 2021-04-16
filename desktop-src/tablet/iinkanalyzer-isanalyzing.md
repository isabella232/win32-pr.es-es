---
description: Recupera un valor que indica si el IInkAnalyzer está realizando el análisis de tinta.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'IInkAnalyzer:: IsAnalyzing (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542011"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="122f4-103">IInkAnalyzer:: IsAnalyzing (método)</span><span class="sxs-lookup"><span data-stu-id="122f4-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="122f4-104">Recupera un valor que indica si el [**IInkAnalyzer**](iinkanalyzer.md) está realizando el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="122f4-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="122f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="122f4-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="122f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="122f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="122f4-107">*pbAnalyzing* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="122f4-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="122f4-108">**Variante \_ TRUE** si [**IInkAnalyzer**](iinkanalyzer.md) está realizando el análisis de tinta; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="122f4-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="122f4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="122f4-109">Return value</span></span>

<span data-ttu-id="122f4-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="122f4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="122f4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="122f4-111">Remarks</span></span>

<span data-ttu-id="122f4-112">Esta propiedad es de **tipo Variant \_ true** si [**IInkAnalyzer**](iinkanalyzer.md) está realizando análisis sincrónicos o asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="122f4-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="122f4-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="122f4-113">Examples</span></span>

<span data-ttu-id="122f4-114">En el ejemplo siguiente se muestra un método que recorre el árbol de resultados [**IContextNode**](icontextnode.md) del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="122f4-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="122f4-115">Si el analizador de tintas no está realizando el análisis de tinta, el método hace lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="122f4-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="122f4-116">Obtiene la cadena de reconocimiento superior.</span><span class="sxs-lookup"><span data-stu-id="122f4-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="122f4-117">Obtiene el nodo raíz del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="122f4-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="122f4-118">Llama a un método auxiliar, `ExploreContextNode` , para examinar el nodo raíz y sus nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="122f4-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="122f4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="122f4-119">Requirements</span></span>



| <span data-ttu-id="122f4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="122f4-120">Requirement</span></span> | <span data-ttu-id="122f4-121">Value</span><span class="sxs-lookup"><span data-stu-id="122f4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122f4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="122f4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="122f4-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="122f4-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="122f4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="122f4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="122f4-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="122f4-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="122f4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="122f4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="122f4-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="122f4-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="122f4-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="122f4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="122f4-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="122f4-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="122f4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="122f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122f4-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="122f4-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="122f4-132">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="122f4-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="122f4-133">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="122f4-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="122f4-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="122f4-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




