---
title: Extensión de clase auxiliar NDF con entrega
description: Esta clase auxiliar tiene una dependencia de mantenimiento bajo en el SimpleFileHelperClass codificado en el primer ejemplo.
ms.assetid: b59cd855-c68a-4f5c-b145-ceac395ddcc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b799b795fcf23cbddf268056e23db433566c8a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994220"
---
# <a name="ndf-helper-class-extension-with-handoff"></a><span data-ttu-id="f9520-103">Extensión de clase auxiliar NDF con entrega</span><span class="sxs-lookup"><span data-stu-id="f9520-103">NDF Helper Class Extension with Handoff</span></span>

<span data-ttu-id="f9520-104">Esta clase auxiliar tiene una dependencia de mantenimiento bajo en el SimpleFileHelperClass codificado en el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f9520-104">This Helper Class has a low-health dependency on the SimpleFileHelperClass coded in the first example.</span></span>

<span data-ttu-id="f9520-105">La segunda clase auxiliar de entrega es una sencilla clase auxiliar de paso a través que no realiza ningún diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f9520-105">The second handoff helper class is a simple pass-through helper class which does not perform any diagnosis itself.</span></span> <span data-ttu-id="f9520-106">En su lugar, siempre genera una hipótesis de mantenimiento inferior para el SimpleFileHelperClass.</span><span class="sxs-lookup"><span data-stu-id="f9520-106">Instead, it always generates lower health hypothesis for the SimpleFileHelperClass.</span></span> <span data-ttu-id="f9520-107">Esto resulta útil para servir como un marcador de posición para futuras adiciones de capacidad de diagnóstico en esta clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f9520-107">This is useful in serving as a placeholder for future addition of diagnostics capability in this helper class.</span></span> <span data-ttu-id="f9520-108">La clase auxiliar de entrega implementa dos métodos.</span><span class="sxs-lookup"><span data-stu-id="f9520-108">The handoff helper class implements two methods.</span></span>

<span data-ttu-id="f9520-109">El método LowHealth se usa para establecer el estado de diagnóstico en DS \_ indeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9520-109">The LowHealth method is used to set the Diagnosis Status to DS\_INDETERMINATE.</span></span> <span data-ttu-id="f9520-110">Esto hace que la llamada NDF GetLowerHypotheses.</span><span class="sxs-lookup"><span data-stu-id="f9520-110">This makes NDF call GetLowerHypotheses.</span></span>


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::LowHealth( 
    /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
    /* [string][out] */ LPWSTR *ppwszDescription,
    /* [out] */ long *pDeferredTime,
    /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    *pStatus = DS_INDETERMINATE;
    return S_OK;
}

```



<span data-ttu-id="f9520-111">A continuación, se implementa GetLowerHypotheses para indicar a NDF la clase auxiliar que se va a diagnosticar.</span><span class="sxs-lookup"><span data-stu-id="f9520-111">Next, GetLowerHypotheses is implemented to tell NDF which Helper Class to diagnose.</span></span>


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::GetLowerHypotheses( 
ULONG *Count,
HYPOTHESIS **Hypotheses)
{
    HRESULT hr = S_OK;
    HYPOTHESIS *pHypothesis=NULL;
    HELPER_ATTRIBUTE *pAttr=NULL;

    pHypothesis = (PHYPOTHESIS)CoTaskMemAlloc(sizeof(HYPOTHESIS));
    if (pHypothesis == NULL)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pHypothesis, sizeof(HYPOTHESIS));

    pAttr = (PHELPER_ATTRIBUTE)CoTaskMemAlloc(sizeof(HELPER_ATTRIBUTE));
    if (pAttr  == NULL)
    {
       hr = E_OUTOFMEMORY;
       goto Error;
    }
    SecureZeroMemory(pAttr, sizeof(HELPER_ATTRIBUTE));

    //set the helper class name to hand off to
    hr = StringCchCopyWithAlloc(&pHypothesis->pwszClassName, MAX_PATH,
                 L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    //populate the attribute
    //set the attribute name
    hr = StringCchCopyWithAlloc(&pAttr->pwszName, MAX_PATH, L"filename");
    if (FAILED(hr))
    {
        goto Error;  
    }

    //set attribute data
    pAttr->type = AT_STRING;
    hr = StringCchCopyWithAlloc(&pAttr->PWStr, MAX_PATH, m_pwszTestFile);
    if (FAILED(hr))
    {
        goto Error;
    }

    //set the attributes to the hypothesis  
    pHypothesis->celt = 1; //number of attributes
    pHypothesis->rgAttributes=pAttr;

    //pass data back
    *pcelt = 1; //one hypothesis
    *pprgHypotheses = pHypothesis;

    return S_OK;

Error:

    if (pAttr)
    {
        if (pAttr->PWStr) 
            CoTaskMemFree(pAttr->PWStr);
        if (pAttr->pwszName) 
            CoTaskMemFree(pAttr->pwszName);
    }

    if (pHypothesis)
    {
        if (pHypothesis->pwszClassName) 
            CoTaskMemFree(pHypothesis->pwszClassName);
        CoTaskMemFree(pHypothesis);
    }
    return hr;
}

```



 

 




