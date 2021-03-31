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
# <a name="registering-a-callback"></a>Registrar una devolución de llamada

Si la aplicación requiere una notificación cuando cambia el valor de una variable de estado o la instancia de servicio que representa deja de estar disponible, la aplicación debe registrar una función de devolución de llamada. Para registrar una función de devolución de llamada para el objeto de servicio que se va a invocar, use el método [**IUPnPService:: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Este método se puede utilizar para registrar más de una devolución de llamada.

Los desarrolladores no deben cancelar una operación asincrónica dentro de una devolución de llamada asincrónica.

> [!Note]  
> Agregar una devolución de llamada en Visual Basic es diferente del método usado en VBScript. La función **GetRef** utilizada en VBScript no está disponible en Visual Basic. Por lo tanto, un desarrollador debe crear un objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenga la función de devolución de llamada como método predeterminado. Vea [registrar una devolución de llamada en Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>Ejemplo de VBScript

El siguiente código de VBScript define la función de devolución de llamada **serviceChangeCallback**, que se invocará cuando cambien los valores de las variables de estado o cuando la instancia de servicio deje de estar disponible. La función tiene cuatro argumentos.

El primer argumento de la función especifica el motivo por el que se invoca la devolución de llamada. Se invoca ya sea porque se ha cambiado una variable de estado o porque la instancia de servicio no está disponible.

El segundo argumento es el objeto de servicio para el que se invoca la devolución de llamada. Si se invoca la devolución de llamada para un cambio de variable de estado, se pasa a la función dos argumentos adicionales: el nombre de la variable que ha cambiado y su nuevo valor.

En este ejemplo, la devolución de llamada simplemente muestra un cuadro de mensaje que muestra el nombre de la variable modificada y su nuevo valor, y si la devolución de llamada se invocó para un cambio de la variable de estado. De lo contrario, muestra un mensaje que indica que la instancia de servicio ya no está disponible.

La última parte del fragmento de código muestra cómo registrar la función de devolución de llamada mediante el método [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Se supone que las variables de objeto de servicio, *appService* y *xportService* se han inicializado, tal y como se muestra en [obtener objetos de servicio](obtaining-service-objects.md).


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



## <a name="c-example"></a>Ejemplo de C++


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



 

 