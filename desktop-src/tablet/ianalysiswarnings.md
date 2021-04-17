---
description: Contiene una colección de objetos que implementan la interfaz IAnalysisWarning y que son el resultado de una operación de análisis de tinta.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Interfaz IAnalysisWarnings (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696542"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="d1c39-103">Interfaz IAnalysisWarnings</span><span class="sxs-lookup"><span data-stu-id="d1c39-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="d1c39-104">Contiene una colección de objetos que implementan la interfaz [**IAnalysisWarning**](ianalysiswarning.md) y que son el resultado de una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="d1c39-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="d1c39-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1c39-105">Members</span></span>

<span data-ttu-id="d1c39-106">La interfaz **IAnalysisWarnings** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d1c39-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d1c39-107">**IAnalysisWarnings** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1c39-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="d1c39-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1c39-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d1c39-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1c39-109">Methods</span></span>

<span data-ttu-id="d1c39-110">La interfaz **IAnalysisWarnings** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d1c39-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="d1c39-111">Método</span><span class="sxs-lookup"><span data-stu-id="d1c39-111">Method</span></span>                                                             | <span data-ttu-id="d1c39-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1c39-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1c39-113">**GetAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="d1c39-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="d1c39-114">Recupera el objeto [**IAnalysisWarning**](ianalysiswarning.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="d1c39-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="d1c39-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="d1c39-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="d1c39-116">Recupera el número de objetos [**IAnalysisWarning**](ianalysiswarning.md) contenidos en la colección **IAnalysisWarnings** .</span><span class="sxs-lookup"><span data-stu-id="d1c39-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="d1c39-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d1c39-117">Examples</span></span>

<span data-ttu-id="d1c39-118">En el ejemplo siguiente se muestra un esquema de un controlador de eventos para el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c39-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="d1c39-119">El controlador comprueba [**IAnalysisStatus:: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="d1c39-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="d1c39-120">Si la operación de análisis generó advertencias, el controlador recorre en iteración la colección de objetos [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c39-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d1c39-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1c39-121">Requirements</span></span>



| <span data-ttu-id="d1c39-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1c39-122">Requirement</span></span> | <span data-ttu-id="d1c39-123">Value</span><span class="sxs-lookup"><span data-stu-id="d1c39-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c39-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1c39-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c39-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d1c39-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1c39-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1c39-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c39-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1c39-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d1c39-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1c39-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1c39-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d1c39-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d1c39-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1c39-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c39-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c39-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d1c39-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1c39-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c39-133">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="d1c39-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="d1c39-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="d1c39-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="d1c39-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d1c39-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

