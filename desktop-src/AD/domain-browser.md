---
title: Explorador de dominio
description: Con la interfaz IDsBrowseDomainTree, una aplicación puede mostrar un cuadro de diálogo del explorador de dominio y obtener el nombre DNS del dominio seleccionado por el usuario.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- AD del explorador de dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338aeb97df8de880fe3b320fed7fbcb3966e7756dd2fe7a16f58f40ccfb69ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018276"
---
# <a name="domain-browser"></a>Explorador de dominio

Con la [**interfaz IDsBrowseDomainTree,**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) una aplicación puede mostrar un cuadro de diálogo del explorador de dominio y obtener el nombre DNS del dominio seleccionado por el usuario. Una aplicación también puede usar la **interfaz IDsBrowseDomainTree** para obtener datos sobre todos los árboles de dominio y dominios dentro de un bosque.

Se crea una instancia de la interfaz [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase **CLSID \_ DsDomainTreeBrowser,** como se muestra a continuación.

El [**método IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) se puede usar para especificar qué equipo y credenciales se usan como base para recuperar los datos de dominio. Cuando se llama a **SetComputer** en una instancia determinada de [**IDsBrowseDomainTree,**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) se debe llamar a [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) antes de volver a llamar a **SetComputer.**

El [**método IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) se usa para mostrar el cuadro de diálogo del explorador de dominio. Cuando el usuario selecciona un dominio  y hace clic en el botón Aceptar, **IDsBrowseDomainTree::BrowseTo** devuelve **S \_ OK** y el parámetro *ppszTargetPath* contiene el nombre del dominio seleccionado. Cuando la cadena de nombre ya no es necesaria, el autor de la llamada debe liberar la cadena llamando a [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

En el ejemplo de código siguiente se muestra cómo usar la interfaz [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) para mostrar el cuadro de diálogo del explorador de dominio.


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



El [**método IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) se usa para obtener datos del árbol de dominio. Los datos de dominio se proporcionan en una [**estructura DOMAINTREE.**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) La **estructura DOMAINTREE** contiene el tamaño de la estructura y el número de elementos de dominio del árbol. La **estructura DOMAINTREE** también contiene una o varias [**estructuras DOMAINDESC.**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) **DOMAINDESC contiene** datos sobre un único elemento del árbol de dominio, incluidos los datos secundarios y del mismo nivel. Los elementos del mismo nivel de un dominio se pueden enumerar accediendo al **miembro pdNextSibling** de cada estructura **DOMAINDESC** posterior. Los secundarios del dominio se pueden recuperar de forma similar accediendo al **miembro pdChildList** de cada estructura **DOMAINDESC** posterior.

En el ejemplo de código siguiente se muestra cómo obtener y acceder a los datos del árbol de dominio mediante el método [**IDsBrowseDomainTree::GetDomains.**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains)


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;

    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);

        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                           dwIndentLevel + 1);
        }
    }
}

//  Entry point for application
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;
        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        pBrowseTree->Release();
    }
    CoUninitialize();
}
```



 

 