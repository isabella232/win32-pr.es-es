---
title: Interfaz IADsObjectOptions
description: La interfaz IADsObjectOptions permite el acceso directo a la configuración y la recuperación de opciones específicas del proveedor.
ms.assetid: b4ac114f-1a23-4be6-af02-0c0d34a8f78f
ms.tgt_platform: multiple
keywords:
- Interfaz IADsObjectOptions ADSI
- IADsObjectOptions ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de IADsObjectOptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049d4dee7f6bf2e7ebb61f01f42ef9fc39271c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993851"
---
# <a name="iadsobjectoptions-interface"></a>Interfaz IADsObjectOptions

La interfaz [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) permite el acceso directo a la configuración y la recuperación de opciones específicas del proveedor.

Una de las opciones del objeto Active Directory es devolver el nombre de host de un servidor. En el ejemplo de código siguiente se usa la interfaz para recuperar el nombre de host del servidor de catálogo global.


```C++
HRESULT GetGCServerName(VARIANT *vGCServer) 
{
    HRESULT hr = S_OK
    HRESULT hre = S_OK;
    IADsContainer *pContainer = NULL;
    IUnknown *pUnk = NULL;
    IEnumVARIANT *pEnum = NULL;
    IDispatch *pDisp = NULL;
    IADsObjectOptions *pOpt = NULL;
    VARIANT var;
    ULONG lFetch = 0;

    VariantInit(&var);
 
    // Bind to the global catalog using a serverless bind.
    hr = ADsOpenObject(L"GC:", NULL, NULL,
                       ADS_SECURE_AUTHENTICATION,
                       IID_IADsContainer, (void**) &pContainer );
    if (FAILED(hr))
        return (hr);
 
    hr = pContainer->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void**) &pEnum);
        if (SUCCEEDED(hr))
        {
            // Enumerate.
            hr = pEnum->Next(1, &var, &lFetch);
            if (SUCCEEDED(hr))
            {
                while (SUCCEEDED(hr))
                {
                    if (lFetch == 1)
                    {
                        pDisp = V_DISPATCH(&var);
                        hre = pDisp->QueryInterface(
                                          IID_IADsObjectOptions,
                                          (void**)&pOpt);
                        if (pDisp)
                            pDisp->Release();
                    }
                    VariantClear(&var);
                    hr = pEnum->Next(1, &var, &lFetch);
                }
                // S_FALSE indicates that the row was read properly.
                if (hr == S_FALSE)
                    hr = hre;
            }
 
            if (SUCCEEDED(hr))
            {
                // There is a valid pOpt, so request the server name.
                VariantInit(vGCServer);
                hr = pOpt->GetOption(ADS_OPTION_SERVERNAME,vGCServer);
            }
        }
    }
 
// Cleanup.
    VariantClear(&var);
    if (pOpt)
        pOpt->Release();
    if (pEnum)
        pEnum->Release();
    if (pUnk)
        pUnk->Release();
    if (pContainer)
        pContainer->Release();
    return (hr);
}
```



 

 




