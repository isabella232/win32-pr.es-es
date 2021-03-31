---
description: Recupera la cadena de resultado mejor de la operación de reconocimiento para todo el árbol de nodos de contexto en el IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'IInkAnalyzer:: GetRecognizedString (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810004"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="84062-103">IInkAnalyzer:: GetRecognizedString (método)</span><span class="sxs-lookup"><span data-stu-id="84062-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="84062-104">Recupera la cadena de resultado mejor de la operación de reconocimiento para todo el árbol de nodos de contexto en el [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="84062-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84062-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84062-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="84062-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84062-107">*pbstrRecognizedString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84062-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84062-108">La cadena de resultado mejor de la operación de reconocimiento para todo el árbol de nodos de contexto en [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="84062-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84062-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84062-109">Return value</span></span>

<span data-ttu-id="84062-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="84062-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="84062-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84062-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="84062-112">Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para *pbstrRecognizedString* cuando ya no necesite usar la cadena.</span><span class="sxs-lookup"><span data-stu-id="84062-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="84062-113">Este método devuelve el mismo valor que los datos de propiedad del nodo raíz para la cadena reconocida.</span><span class="sxs-lookup"><span data-stu-id="84062-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="84062-114">(Consulte el [**método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md), [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)y [las propiedades del nodo de contexto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="84062-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="84062-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="84062-115">Examples</span></span>

<span data-ttu-id="84062-116">En el ejemplo siguiente se muestra un método que recorre el árbol de resultados [**IContextNode**](icontextnode.md) del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="84062-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="84062-117">Si el IInkAnlyzer no está realizando actualmente el análisis de tinta, el método hace lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="84062-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="84062-118">Obtiene la cadena de reconocimiento superior.</span><span class="sxs-lookup"><span data-stu-id="84062-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="84062-119">Obtiene el nodo raíz del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="84062-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="84062-120">Llama a un método auxiliar, `ExploreContextNode` , para examinar el nodo raíz y sus nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="84062-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="84062-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84062-121">Requirements</span></span>



| <span data-ttu-id="84062-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="84062-122">Requirement</span></span> | <span data-ttu-id="84062-123">Value</span><span class="sxs-lookup"><span data-stu-id="84062-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84062-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84062-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84062-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="84062-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="84062-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84062-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84062-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="84062-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="84062-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84062-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="84062-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="84062-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="84062-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84062-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84062-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84062-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="84062-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="84062-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84062-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="84062-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="84062-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="84062-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

