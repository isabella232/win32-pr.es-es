---
title: Explorador de dominio
description: Mediante la interfaz IDsBrowseDomainTree, una aplicación puede mostrar un cuadro de diálogo de explorador de dominio y obtener el nombre DNS del dominio seleccionado por el usuario.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- AD del explorador de dominios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077525"
---
# <a name="domain-browser"></a><span data-ttu-id="1e03d-104">Explorador de dominio</span><span class="sxs-lookup"><span data-stu-id="1e03d-104">Domain Browser</span></span>

<span data-ttu-id="1e03d-105">Mediante la interfaz [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , una aplicación puede mostrar un cuadro de diálogo de explorador de dominio y obtener el nombre DNS del dominio seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1e03d-105">Using the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface, an application can display a domain browser dialog box and obtain the DNS name of the domain selected by the user.</span></span> <span data-ttu-id="1e03d-106">Una aplicación también puede utilizar la interfaz **IDsBrowseDomainTree** para obtener datos sobre todos los árboles de dominio y dominios de un bosque.</span><span class="sxs-lookup"><span data-stu-id="1e03d-106">An application can also use the **IDsBrowseDomainTree** interface to obtain data about all domain trees and domains within a forest.</span></span>

<span data-ttu-id="1e03d-107">Una instancia de la interfaz [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) se crea llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase **\_ DsDomainTreeBrowser CLSID** , como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="1e03d-107">An instance of the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface is created by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsDomainTreeBrowser** class identifier as shown below.</span></span>

<span data-ttu-id="1e03d-108">El método [**IDsBrowseDomainTree:: SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) se puede usar para especificar el equipo y las credenciales que se usan como base para recuperar los datos del dominio.</span><span class="sxs-lookup"><span data-stu-id="1e03d-108">The [**IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) method can be used to specify which computer and credentials are used as the basis for retrieving the domain data.</span></span> <span data-ttu-id="1e03d-109">Cuando se llama a **SetComputer** en una instancia de [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) determinada, se debe llamar a [**IDsBrowseDomainTree:: FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) antes de volver a llamar a **SetComputer** .</span><span class="sxs-lookup"><span data-stu-id="1e03d-109">When **SetComputer** is called on a particular [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) instance, [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) must be called before **SetComputer** is called again.</span></span>

<span data-ttu-id="1e03d-110">El método [**IDsBrowseDomainTree:: browseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) se usa para mostrar el cuadro de diálogo explorador de dominio.</span><span class="sxs-lookup"><span data-stu-id="1e03d-110">The [**IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) method is used to display the domain browser dialog box.</span></span> <span data-ttu-id="1e03d-111">Cuando el usuario selecciona un dominio y hace clic en el botón **Aceptar** , **IDsBrowseDomainTree:: browseTo** devuelve **S \_ OK** y el parámetro *ppszTargetPath* contiene el nombre del dominio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1e03d-111">When the user selects a domain and clicks the **OK** button, the **IDsBrowseDomainTree::BrowseTo** returns **S\_OK** and the *ppszTargetPath* parameter contains the name of the selected domain.</span></span> <span data-ttu-id="1e03d-112">Cuando la cadena de nombre ya no es necesaria, el llamador debe liberar la cadena mediante una llamada a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="1e03d-112">When the name string is no longer required, the caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

<span data-ttu-id="1e03d-113">En el ejemplo de código siguiente se muestra cómo utilizar la interfaz [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) para mostrar el cuadro de diálogo explorador de dominio.</span><span class="sxs-lookup"><span data-stu-id="1e03d-113">The following code example shows how to use the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface to display the domain browser dialog box.</span></span>


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



<span data-ttu-id="1e03d-114">El método [**IDsBrowseDomainTree:: GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) se usa para obtener los datos del árbol de dominios.</span><span class="sxs-lookup"><span data-stu-id="1e03d-114">The [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method is used to obtain domain tree data.</span></span> <span data-ttu-id="1e03d-115">Los datos de dominio se proporcionan en una estructura [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) .</span><span class="sxs-lookup"><span data-stu-id="1e03d-115">The domain data is supplied in a [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) structure.</span></span> <span data-ttu-id="1e03d-116">La estructura **DOMAINTREE** contiene el tamaño de la estructura y el número de elementos de dominio en el árbol.</span><span class="sxs-lookup"><span data-stu-id="1e03d-116">The **DOMAINTREE** structure contains the size of the structure and the number of domain elements in the tree.</span></span> <span data-ttu-id="1e03d-117">La estructura **DOMAINTREE** también contiene una o varias estructuras [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) .</span><span class="sxs-lookup"><span data-stu-id="1e03d-117">The **DOMAINTREE** structure also contains one or more [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) structures.</span></span> <span data-ttu-id="1e03d-118">**DOMAINDESC** contiene datos sobre un elemento único en el árbol de dominios, incluidos los datos secundarios y los elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1e03d-118">The **DOMAINDESC** contains data about a single element in the domain tree, including child and sibling data.</span></span> <span data-ttu-id="1e03d-119">Los elementos del mismo nivel de un dominio se pueden enumerar accediendo al miembro **pdNextSibling** de cada estructura **DOMAINDESC** subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="1e03d-119">The siblings of a domain can be enumerated by accessing the **pdNextSibling** member of each subsequent **DOMAINDESC** structure.</span></span> <span data-ttu-id="1e03d-120">Los elementos secundarios del dominio se pueden recuperar de forma similar accediendo al miembro **pdChildList** de cada estructura **DOMAINDESC** subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="1e03d-120">The children of the domain can be retrieved in a similar manner by accessing the **pdChildList** member of each subsequent **DOMAINDESC** structure.</span></span>

<span data-ttu-id="1e03d-121">En el ejemplo de código siguiente se muestra cómo obtener y obtener acceso a los datos del árbol de dominios mediante el método [**IDsBrowseDomainTree:: GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) .</span><span class="sxs-lookup"><span data-stu-id="1e03d-121">The following code example shows how to obtain and access the domain tree data using the [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method.</span></span>


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



 

 