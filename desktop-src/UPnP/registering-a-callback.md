---
title: Registrar una devolución de llamada
description: Si la aplicación requiere una notificación cuando cambia el valor de una variable de estado o la instancia de servicio que representa deja de estar disponible, la aplicación debe registrar una función de devolución de llamada.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792220"
---
# <a name="registering-a-callback"></a><span data-ttu-id="e78e2-103">Registrar una devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="e78e2-103">Registering a Callback</span></span>

<span data-ttu-id="e78e2-104">Si la aplicación requiere una notificación cuando cambia el valor de una variable de estado o la instancia de servicio que representa deja de estar disponible, la aplicación debe registrar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e78e2-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="e78e2-105">Para registrar una función de devolución de llamada para el objeto de servicio que se va a invocar, use el método [**IUPnPService:: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="e78e2-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="e78e2-106">Este método se puede utilizar para registrar más de una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e78e2-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="e78e2-107">Los desarrolladores no deben cancelar una operación asincrónica dentro de una devolución de llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e78e2-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="e78e2-108">Agregar una devolución de llamada en Visual Basic es diferente del método usado en VBScript.</span><span class="sxs-lookup"><span data-stu-id="e78e2-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="e78e2-109">La función **GetRef** utilizada en VBScript no está disponible en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e78e2-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="e78e2-110">Por lo tanto, un desarrollador debe crear un objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenga la función de devolución de llamada como método predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e78e2-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="e78e2-111">Vea [registrar una devolución de llamada en Visual Basic](registering-a-callback-in-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="e78e2-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="e78e2-112">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="e78e2-112">VBScript Example</span></span>

<span data-ttu-id="e78e2-113">El siguiente código de VBScript define la función de devolución de llamada **serviceChangeCallback**, que se invocará cuando cambien los valores de las variables de estado o cuando la instancia de servicio deje de estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e78e2-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="e78e2-114">La función tiene cuatro argumentos.</span><span class="sxs-lookup"><span data-stu-id="e78e2-114">The function has four arguments.</span></span>

<span data-ttu-id="e78e2-115">El primer argumento de la función especifica el motivo por el que se invoca la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e78e2-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="e78e2-116">Se invoca ya sea porque se ha cambiado una variable de estado o porque la instancia de servicio no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e78e2-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="e78e2-117">El segundo argumento es el objeto de servicio para el que se invoca la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e78e2-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="e78e2-118">Si se invoca la devolución de llamada para un cambio de variable de estado, se pasa a la función dos argumentos adicionales: el nombre de la variable que ha cambiado y su nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="e78e2-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="e78e2-119">En este ejemplo, la devolución de llamada simplemente muestra un cuadro de mensaje que muestra el nombre de la variable modificada y su nuevo valor, y si la devolución de llamada se invocó para un cambio de la variable de estado.</span><span class="sxs-lookup"><span data-stu-id="e78e2-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="e78e2-120">De lo contrario, muestra un mensaje que indica que la instancia de servicio ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e78e2-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="e78e2-121">La última parte del fragmento de código muestra cómo registrar la función de devolución de llamada mediante el método [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="e78e2-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="e78e2-122">Se supone que las variables de objeto de servicio, *appService* y *xportService* se han inicializado, tal y como se muestra en [obtener objetos de servicio](obtaining-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e78e2-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a><span data-ttu-id="e78e2-123">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="e78e2-123">C++ Example</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 