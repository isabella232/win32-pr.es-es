---
title: Enlazar a objetos secundarios
description: En ADSI, un objeto contenedor expone la interfaz IADsContainer.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, enlazar a objetos secundarios
- Enlazar a objetos secundarios
- Objetos secundarios, enlazar a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488267"
---
# <a name="binding-to-child-objects"></a>Enlazar a objetos secundarios

En ADSI, un objeto contenedor expone la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . El método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) se utiliza para enlazar directamente a un objeto secundario. El objeto devuelto por **IADsContainer:: GetObject** tiene el mismo contexto de seguridad que el objeto en el que se llamó al método. Esto significa que, si se usan credenciales alternativas, las credenciales alternativas no tienen que pasarse de nuevo a la función de enlace o al método para mantener las mismas credenciales.

El método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) toma un nombre distintivo relativo (RDN) que es relativo al objeto actual. Este método también toma un nombre de clase opcional y devuelve un puntero de interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que representa el objeto secundario. Para obtener la interfaz ADSI deseada, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), llame al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de este puntero de interfaz **IDispatch** .

En el ejemplo de código de C++ siguiente se muestra una función que recupera un objeto secundario especificado.


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 