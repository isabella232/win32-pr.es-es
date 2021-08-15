---
title: Código de ejemplo para buscar un bosque
description: Este tema contiene código de ejemplo que busca en un bosque.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , buscar en un bosque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92c71afeecebf96ba123e909ad408835de083b8d45cb259a7b371b8214cc5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190292"
---
# <a name="example-code-for-searching-a-forest"></a>Código de ejemplo para buscar un bosque

Este tema contiene código de ejemplo que busca en un bosque.

En el siguiente ejemplo de código de C/C++ se enlaza a la raíz del catálogo global y se enumera el objeto único, que es la raíz del bosque, para que se pueda usar para buscar en todo el bosque.


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



El siguiente ejemplo de código de C/C++ contiene una función que devuelve un [**puntero IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usado para buscar en todo el bosque.

La función realiza un enlace sin servidor a la raíz del catálogo global, enumera el único elemento, que es la raíz del bosque y se puede usar para buscar en todo el bosque, llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) al objeto y devuelve ese puntero para que lo use el autor de la llamada para buscar en el bosque.


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



 

 