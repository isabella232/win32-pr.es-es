---
description: Representa una advertencia o un error que se produce durante una operación de análisis de tinta.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interfaz IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154445"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="bef54-103">Interfaz IAnalysisWarning</span><span class="sxs-lookup"><span data-stu-id="bef54-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="bef54-104">Representa una advertencia o un error que se produce durante una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="bef54-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="bef54-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="bef54-105">Members</span></span>

<span data-ttu-id="bef54-106">La interfaz **IAnalysisWarning** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bef54-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bef54-107">**IAnalysisWarning** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bef54-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="bef54-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="bef54-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bef54-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="bef54-109">Methods</span></span>

<span data-ttu-id="bef54-110">La interfaz **IAnalysisWarning** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bef54-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="bef54-111">Método</span><span class="sxs-lookup"><span data-stu-id="bef54-111">Method</span></span>                                                            | <span data-ttu-id="bef54-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bef54-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bef54-113">**GetBackgroundError**</span><span class="sxs-lookup"><span data-stu-id="bef54-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="bef54-114">Recupera el código de error de la operación de análisis de tinta de fondo si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="bef54-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="bef54-115">**GetHint**</span><span class="sxs-lookup"><span data-stu-id="bef54-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="bef54-116">Recupera la sugerencia de análisis que produjo esta advertencia</span><span class="sxs-lookup"><span data-stu-id="bef54-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="bef54-117">**GetNodeIds**</span><span class="sxs-lookup"><span data-stu-id="bef54-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="bef54-118">Recupera los identificadores de los nodos de contexto pertinentes que están asociados a esta advertencia.</span><span class="sxs-lookup"><span data-stu-id="bef54-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="bef54-119">**GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="bef54-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="bef54-120">Recupera el tipo de advertencia que se produjo mediante la enumeración [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="bef54-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bef54-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bef54-121">Remarks</span></span>

<span data-ttu-id="bef54-122">Los tipos de advertencias que se pueden producir se describen en la enumeración [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="bef54-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="bef54-123">A menudo se producen advertencias al intentar usar una característica que no es compatible con el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que usa [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="bef54-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="bef54-124">Algunas advertencias indican que el [**IInkAnalyzer**](iinkanalyzer.md) no completó la operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="bef54-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="bef54-125">Para obtener más información, vea [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span><span class="sxs-lookup"><span data-stu-id="bef54-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="bef54-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bef54-126">Examples</span></span>

<span data-ttu-id="bef54-127">En el ejemplo siguiente se muestra un esquema de un controlador de eventos para el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="bef54-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="bef54-128">El controlador comprueba [**IAnalysisStatus:: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="bef54-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="bef54-129">Si la operación de análisis genera advertencias, el controlador recorre en iteración la colección de objetos **IAnalysisWarning** .</span><span class="sxs-lookup"><span data-stu-id="bef54-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="bef54-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef54-130">Requirements</span></span>



| <span data-ttu-id="bef54-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef54-131">Requirement</span></span> | <span data-ttu-id="bef54-132">Value</span><span class="sxs-lookup"><span data-stu-id="bef54-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef54-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef54-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bef54-134">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bef54-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bef54-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef54-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bef54-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bef54-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bef54-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bef54-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef54-138"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bef54-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bef54-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bef54-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bef54-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bef54-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bef54-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="bef54-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef54-142">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="bef54-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="bef54-143">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="bef54-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="bef54-144">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="bef54-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

