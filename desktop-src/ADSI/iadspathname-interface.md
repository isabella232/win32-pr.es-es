---
title: Interfaz IADsPathname
description: Analiza y modifica varios elementos de una ADsPath.
ms.assetid: 1f820488-2e75-4257-90c7-9ec67aac4fe4
ms.tgt_platform: multiple
keywords:
- Interfaz IADsPathname ADSI
- IADsPathname ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de IADsPathname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5cbc5901c8f9dcebebde485decc49fc5bcf312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903048"
---
# <a name="iadspathname-interface"></a><span data-ttu-id="99e97-106">Interfaz IADsPathname</span><span class="sxs-lookup"><span data-stu-id="99e97-106">IADsPathname Interface</span></span>

<span data-ttu-id="99e97-107">La interfaz [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) analiza y modifica varios elementos de una ADsPath.</span><span class="sxs-lookup"><span data-stu-id="99e97-107">The [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface parses and modifies various elements of an ADsPath.</span></span> <span data-ttu-id="99e97-108">También convierte ADsPaths entre varios formatos de presentación.</span><span class="sxs-lookup"><span data-stu-id="99e97-108">It also converts ADsPaths between various display formats.</span></span>

<span data-ttu-id="99e97-109">En el ejemplo de código siguiente se extrae y se devuelve el nombre del servidor de una ADsPath válida para que se muestre al usuario en una utilidad de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="99e97-109">The following code example extracts and returns the server name from a valid ADsPath for display to the user in a maintenance utility.</span></span>


```C++
HRESULT GetServerName(BSTR adsPath, BSTR *adsServer)
{
    HRESULT hr = S_OK;
    IADsPathname *pIADsPathname = NULL;
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
 
    // Set the path.
    hr = pIADsPathname->Set(adsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
        // Extract and return the server name.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_SERVER, adsServer);
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
}
```



<span data-ttu-id="99e97-110">El siguiente ejemplo de código ayuda a inicializar un objeto ADSI recién creado estableciendo la propiedad **nombre distintivo** del objeto desde su propio ADsPath.</span><span class="sxs-lookup"><span data-stu-id="99e97-110">The following code example helps to initialize a newly created ADSI object by setting the object's **Distinguished Name** property from its own ADsPath.</span></span> <span data-ttu-id="99e97-111">Tenga en cuenta que la rutina que realiza la llamada debe confirmar los cambios en el almacén de directorios subyacente mediante la invocación del método **SetInfo** .</span><span class="sxs-lookup"><span data-stu-id="99e97-111">Be aware that the calling routine must commit any changes to the underlying directory store by invoking the **SetInfo** method.</span></span>


```C++
HRESULT SetDistinguishedName(IADs *pIADs)
{
    HRESULT hr = S_OK;
    CComBSTR sbstrADsPath;
    IADsPathname *pIADsPathname = NULL;
 
    // Get the ADsPath for this object.
    hr = pIADs->get_ADsPath(&sbstrADsPath);
    if (FAILED(hr))
        return (hr);
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
     // Set the path.
    hr = pIADsPathname->Set(sbstrADsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
    {
        CComBSTR sbstrDNPath;

        // Convert the path to Distinguished Name format.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,
                                     &sbstrDNPath);
 
        if (SUCCEEDED(hr))
        {
            // Set the distinguished name property.
            VARIANT var;
            VariantInit(&var);
            V_BSTR(&var) = sbstrDNPath;
            V_VT(&var) = VT_BSTR;
            hr = pIADs->Put(CComBSTR("distinguishedName"), var);
            VariantClear(&var);
        }
    }
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
 
}
```



 

 




