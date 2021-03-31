---
title: Código de ejemplo para buscar en un bosque
description: Este tema contiene código de ejemplo que busca en un bosque.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, buscar en un bosque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c2fb0cde0f42167b19141ad178ea80ff8795b8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789544"
---
# <a name="example-code-for-searching-a-forest"></a><span data-ttu-id="96119-104">Código de ejemplo para buscar en un bosque</span><span class="sxs-lookup"><span data-stu-id="96119-104">Example Code for Searching a Forest</span></span>

<span data-ttu-id="96119-105">Este tema contiene código de ejemplo que busca en un bosque.</span><span class="sxs-lookup"><span data-stu-id="96119-105">This topic contains example code that searches a forest.</span></span>

<span data-ttu-id="96119-106">El siguiente ejemplo de código de C/C++ enlaza con la raíz del catálogo global y enumera el objeto único, que es la raíz del bosque, para que se pueda usar para buscar en todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="96119-106">The following C/C++ code example binds to the root of the Global Catalog and enumerates the single object, which is the root of the forest, so that it can be used to search the entire forest.</span></span>


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



<span data-ttu-id="96119-107">El siguiente ejemplo de código de C/C++ contiene una función que devuelve un puntero [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que se usa para buscar en todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="96119-107">The following C/C++ code example contains a function that returns an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer used to search the entire forest.</span></span>

<span data-ttu-id="96119-108">La función realiza un enlace sin servidor a la raíz del catálogo global, enumera el elemento único, que es la raíz del bosque y se puede usar para buscar en todo el bosque, llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) al objeto y devuelve ese puntero para que el llamador lo use para buscar en el bosque.</span><span class="sxs-lookup"><span data-stu-id="96119-108">The function performs a serverless bind to the root of the Global Catalog, enumerates the single item, which is the root of the forest and can be used to search the entire forest, calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer to the object, and returns that pointer for use by the caller to search the forest.</span></span>


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 