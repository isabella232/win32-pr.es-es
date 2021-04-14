---
title: Invocar acciones
description: El método IUPnPService InvokeAction permite invocar acciones en los objetos de servicio.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421157"
---
# <a name="invoking-actions"></a>Invocar acciones

El método [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) permite invocar acciones en los objetos de servicio. Este método tiene dos parámetros de entrada: el nombre de una acción y una matriz de argumentos de entrada para esa acción. El método tiene dos parámetros:

-   Parámetro uno: un parámetro de entrada/salida: una matriz de argumentos de salida para esa acción.
-   Parámetro dos: un parámetro de salida: un valor devuelto.

El método hace que la acción se invoque en el dispositivo. El dispositivo genera notificaciones de eventos si la acción hace que las variables de estado del dispositivo cambien.

## <a name="vbscript-example"></a>Ejemplo de VBScript

En el siguiente ejemplo de código de VBScript se invocan dos acciones en un objeto de servicio. La primera acción, *GetTrackInfo*, toma un argumento de entrada, un número de pista. La acción *GetTrackInfo* devuelve la longitud de la pista como el valor devuelto. La acción también tiene un argumento de salida, que contiene el título de la pista si el método devuelve SUCCESS.

Después de invocar la acción *GetTrackInfo* , el ejemplo invoca la acción Play, que no toma ningún argumento. Sin embargo, dado que la sintaxis de [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiere una matriz de argumentos de entrada y de salida, el ejemplo debe crear una matriz vacía, *emptyArgs*, sin elementos. En el ejemplo se pasa esta matriz a **InvokeAction** para los argumentos de entrada y salida, junto con el nombre de la acción.


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a>Ejemplo de C++

En el ejemplo siguiente se define una función de C++ que invoca una acción sin argumentos. Dado que [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiere que se pase un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de argumentos, este ejemplo crea una **SAFEARRAY** vacía. Dado que esta acción no devuelve un valor o tiene argumentos de salida, en este ejemplo se omiten los dos últimos valores de [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) pasados a **InvokeAction**.

El dispositivo genera notificaciones de eventos si la acción hace que las variables de estado del dispositivo cambien.


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



En el ejemplo siguiente se invoca la acción ficticia *GetTrackInfo* . Toma un número de pista como argumento, devuelve la longitud de la pista como un valor devuelto y devuelve el título de la pista en un argumento de salida. El código es similar al ejemplo anterior, salvo que en lugar de crear una [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) vacía de argumentos de entrada, en este ejemplo se inserta una [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) que contiene el número de pista. Si [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) devuelve Success, en este ejemplo se examina el valor devuelto y la matriz de argumentos de salida.


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 