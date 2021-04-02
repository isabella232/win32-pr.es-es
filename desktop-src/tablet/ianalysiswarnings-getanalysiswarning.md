---
description: Recupera el objeto IAnalysisWarning en el índice especificado.
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'IAnalysisWarnings:: GetAnalysisWarning (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082159"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="fae03-103">IAnalysisWarnings:: GetAnalysisWarning (método)</span><span class="sxs-lookup"><span data-stu-id="fae03-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="fae03-104">Recupera el objeto [**IAnalysisWarning**](ianalysiswarning.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fae03-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fae03-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="fae03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fae03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae03-107">*ulIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fae03-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae03-108">Índice de base cero del objeto [**IAnalysisWarning**](ianalysiswarning.md) que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="fae03-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="fae03-109">*ppWarning* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fae03-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fae03-110">Puntero al objeto [**IAnalysisWarning**](ianalysiswarning.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fae03-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae03-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fae03-111">Return value</span></span>

<span data-ttu-id="fae03-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fae03-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fae03-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fae03-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fae03-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppWarning* cuando ya no necesite usar la advertencia.</span><span class="sxs-lookup"><span data-stu-id="fae03-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fae03-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fae03-115">Examples</span></span>

<span data-ttu-id="fae03-116">En el ejemplo siguiente se muestra un esquema de un controlador de eventos para el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="fae03-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="fae03-117">El controlador comprueba [**IAnalysisStatus:: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="fae03-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="fae03-118">Si la operación de análisis genera advertencias, el controlador recorre en iteración la colección de objetos [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="fae03-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fae03-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae03-119">Requirements</span></span>



| <span data-ttu-id="fae03-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae03-120">Requirement</span></span> | <span data-ttu-id="fae03-121">Value</span><span class="sxs-lookup"><span data-stu-id="fae03-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae03-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae03-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fae03-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fae03-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fae03-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae03-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fae03-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fae03-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fae03-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fae03-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae03-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fae03-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fae03-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fae03-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae03-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae03-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fae03-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fae03-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae03-131">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="fae03-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="fae03-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="fae03-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

