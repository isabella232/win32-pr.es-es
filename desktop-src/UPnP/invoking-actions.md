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
# <a name="invoking-actions"></a><span data-ttu-id="45e86-103">Invocar acciones</span><span class="sxs-lookup"><span data-stu-id="45e86-103">Invoking Actions</span></span>

<span data-ttu-id="45e86-104">El método [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) permite invocar acciones en los objetos de servicio.</span><span class="sxs-lookup"><span data-stu-id="45e86-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="45e86-105">Este método tiene dos parámetros de entrada: el nombre de una acción y una matriz de argumentos de entrada para esa acción.</span><span class="sxs-lookup"><span data-stu-id="45e86-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="45e86-106">El método tiene dos parámetros:</span><span class="sxs-lookup"><span data-stu-id="45e86-106">The method has two parameters:</span></span>

-   <span data-ttu-id="45e86-107">Parámetro uno: un parámetro de entrada/salida: una matriz de argumentos de salida para esa acción.</span><span class="sxs-lookup"><span data-stu-id="45e86-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="45e86-108">Parámetro dos: un parámetro de salida: un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="45e86-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="45e86-109">El método hace que la acción se invoque en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45e86-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="45e86-110">El dispositivo genera notificaciones de eventos si la acción hace que las variables de estado del dispositivo cambien.</span><span class="sxs-lookup"><span data-stu-id="45e86-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="45e86-111">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="45e86-111">VBScript Example</span></span>

<span data-ttu-id="45e86-112">En el siguiente ejemplo de código de VBScript se invocan dos acciones en un objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="45e86-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="45e86-113">La primera acción, *GetTrackInfo*, toma un argumento de entrada, un número de pista.</span><span class="sxs-lookup"><span data-stu-id="45e86-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="45e86-114">La acción *GetTrackInfo* devuelve la longitud de la pista como el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="45e86-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="45e86-115">La acción también tiene un argumento de salida, que contiene el título de la pista si el método devuelve SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="45e86-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="45e86-116">Después de invocar la acción *GetTrackInfo* , el ejemplo invoca la acción Play, que no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="45e86-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="45e86-117">Sin embargo, dado que la sintaxis de [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiere una matriz de argumentos de entrada y de salida, el ejemplo debe crear una matriz vacía, *emptyArgs*, sin elementos.</span><span class="sxs-lookup"><span data-stu-id="45e86-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="45e86-118">En el ejemplo se pasa esta matriz a **InvokeAction** para los argumentos de entrada y salida, junto con el nombre de la acción.</span><span class="sxs-lookup"><span data-stu-id="45e86-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


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



## <a name="c-example"></a><span data-ttu-id="45e86-119">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="45e86-119">C++ Example</span></span>

<span data-ttu-id="45e86-120">En el ejemplo siguiente se define una función de C++ que invoca una acción sin argumentos.</span><span class="sxs-lookup"><span data-stu-id="45e86-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="45e86-121">Dado que [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiere que se pase un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de argumentos, este ejemplo crea una **SAFEARRAY** vacía.</span><span class="sxs-lookup"><span data-stu-id="45e86-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="45e86-122">Dado que esta acción no devuelve un valor o tiene argumentos de salida, en este ejemplo se omiten los dos últimos valores de [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) pasados a **InvokeAction**.</span><span class="sxs-lookup"><span data-stu-id="45e86-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="45e86-123">El dispositivo genera notificaciones de eventos si la acción hace que las variables de estado del dispositivo cambien.</span><span class="sxs-lookup"><span data-stu-id="45e86-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


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



<span data-ttu-id="45e86-124">En el ejemplo siguiente se invoca la acción ficticia *GetTrackInfo* .</span><span class="sxs-lookup"><span data-stu-id="45e86-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="45e86-125">Toma un número de pista como argumento, devuelve la longitud de la pista como un valor devuelto y devuelve el título de la pista en un argumento de salida.</span><span class="sxs-lookup"><span data-stu-id="45e86-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="45e86-126">El código es similar al ejemplo anterior, salvo que en lugar de crear una [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) vacía de argumentos de entrada, en este ejemplo se inserta una [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) que contiene el número de pista.</span><span class="sxs-lookup"><span data-stu-id="45e86-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="45e86-127">Si [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) devuelve Success, en este ejemplo se examina el valor devuelto y la matriz de argumentos de salida.</span><span class="sxs-lookup"><span data-stu-id="45e86-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


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



 

 