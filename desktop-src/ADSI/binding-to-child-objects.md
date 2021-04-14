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
# <a name="binding-to-child-objects"></a><span data-ttu-id="789a7-106">Enlazar a objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="789a7-106">Binding to Child Objects</span></span>

<span data-ttu-id="789a7-107">En ADSI, un objeto contenedor expone la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="789a7-107">In ADSI, a container object exposes the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span> <span data-ttu-id="789a7-108">El método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) se utiliza para enlazar directamente a un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="789a7-108">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method is used to bind directly to a child object.</span></span> <span data-ttu-id="789a7-109">El objeto devuelto por **IADsContainer:: GetObject** tiene el mismo contexto de seguridad que el objeto en el que se llamó al método.</span><span class="sxs-lookup"><span data-stu-id="789a7-109">The object returned by **IADsContainer::GetObject** has the same security context as the object on which the method was called.</span></span> <span data-ttu-id="789a7-110">Esto significa que, si se usan credenciales alternativas, las credenciales alternativas no tienen que pasarse de nuevo a la función de enlace o al método para mantener las mismas credenciales.</span><span class="sxs-lookup"><span data-stu-id="789a7-110">This means that if alternate credentials are used, the alternate credentials do not have to be passed to the binding function or method again to maintain the same credentials.</span></span>

<span data-ttu-id="789a7-111">El método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) toma un nombre distintivo relativo (RDN) que es relativo al objeto actual.</span><span class="sxs-lookup"><span data-stu-id="789a7-111">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method takes a relative distinguished name (RDN) that is relative to the current object.</span></span> <span data-ttu-id="789a7-112">Este método también toma un nombre de clase opcional y devuelve un puntero de interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que representa el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="789a7-112">This method also takes an optional class name and returns an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface pointer that represents the child object.</span></span> <span data-ttu-id="789a7-113">Para obtener la interfaz ADSI deseada, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), llame al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de este puntero de interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="789a7-113">To obtain the desired ADSI interface, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of this **IDispatch** interface pointer.</span></span>

<span data-ttu-id="789a7-114">En el ejemplo de código de C++ siguiente se muestra una función que recupera un objeto secundario especificado.</span><span class="sxs-lookup"><span data-stu-id="789a7-114">The following C++ code example shows a function that retrieves a specified child object.</span></span>


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



 

 