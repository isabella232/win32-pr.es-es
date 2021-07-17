---
title: XInput y DirectInput
description: XInput es una API que permite a las aplicaciones recibir entradas del controlador de Xbox para Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373190"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="ea3f4-103">XInput y DirectInput</span><span class="sxs-lookup"><span data-stu-id="ea3f4-103">XInput and DirectInput</span></span>

<span data-ttu-id="ea3f4-104">XInput es una API que permite a las aplicaciones recibir entradas del controlador de Xbox para Windows.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="ea3f4-105">En este documento se describen las diferencias entre las implementaciones de XInput y [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controlador de Xbox y cómo puede admitir dispositivos XInput y dispositivos DirectInput heredados al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="ea3f4-106">No se recomienda el [uso de DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredado y DirectInput no está disponible para Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="ea3f4-107">El nuevo estándar: XInput</span><span class="sxs-lookup"><span data-stu-id="ea3f4-107">The New Standard: XInput</span></span>

<span data-ttu-id="ea3f4-108">XInput ya está disponible para el desarrollo de juegos.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-108">XInput is now available for game development.</span></span> <span data-ttu-id="ea3f4-109">Este es el nuevo estándar de entrada para Xbox y Windows.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="ea3f4-110">Las API están disponibles a través del SDK de DirectX y el controlador está disponible a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="ea3f4-111">El uso de XInput sobre DirectInput tiene varias [ventajas:](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea3f4-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="ea3f4-112">XInput es más fácil de usar y requiere menos configuración que [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea3f4-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="ea3f4-113">Tanto Xbox como Windows programación usarán los mismos conjuntos de API principales, lo que permite que la programación traduzca la multiplataforma mucho más fácil.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="ea3f4-114">Habrá una gran base instalada de controladores de Xbox.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="ea3f4-115">Los dispositivos XInput (es decir, los controladores de Xbox) solo tendrán funcionalidad de vibración cuando se usen las API XInput.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="ea3f4-116">Los controladores futuros publicados para la consola Xbox (es decir, las ruedas de ruedas) también funcionarán en Windows</span><span class="sxs-lookup"><span data-stu-id="ea3f4-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="ea3f4-117">Uso del controlador xbox con DirectInput</span><span class="sxs-lookup"><span data-stu-id="ea3f4-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="ea3f4-118">El controlador de Xbox se enumera correctamente en [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))y se puede usar con directInputAPIs.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="ea3f4-119">Sin embargo, faltará alguna funcionalidad proporcionada por XInput en la implementación de DirectInput:</span><span class="sxs-lookup"><span data-stu-id="ea3f4-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="ea3f4-120">Los botones de desencadenador izquierdo y derecho actuarán como un botón único, no de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="ea3f4-121">Los efectos de vibración no estarán disponibles</span><span class="sxs-lookup"><span data-stu-id="ea3f4-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="ea3f4-122">Las consultas de dispositivos de casco no estarán disponibles</span><span class="sxs-lookup"><span data-stu-id="ea3f4-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="ea3f4-123">La combinación de los desencadenadores izquierdo y derecho [en DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) es por diseño.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="ea3f4-124">Los juegos siempre han asumido que los ejes del dispositivo DirectInput están centrados cuando no hay ninguna interacción del usuario con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="ea3f4-125">Sin embargo, el controlador de Xbox se diseñó para registrar el valor mínimo, no el centro, cuando no se mantienen los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="ea3f4-126">Por lo tanto, los juegos más antiguos asumirían la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="ea3f4-127">La solución era combinar los desencadenadores, estableciendo un desencadenador en una dirección positiva y el otro en una dirección negativa, por lo que ninguna interacción del usuario es indicativa a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) de que el "control" está en el centro.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="ea3f4-128">Para probar los valores del desencadenador por separado, debe usar XInput.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="ea3f4-129">XInput y DirectInput en paralelo</span><span class="sxs-lookup"><span data-stu-id="ea3f4-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="ea3f4-130">Al admitir solo XInput, el juego no funcionará con dispositivos [DirectInput heredados.](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea3f4-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="ea3f4-131">XInput no reconocerá estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="ea3f4-132">Si quiere que el juego admita dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredados, puede usar DirectInput y XInput en paralelo.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="ea3f4-133">Al enumerar los dispositivos DirectInput, todos los dispositivos DirectInput se enumerarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="ea3f4-134">Todos los dispositivos XInput se mostrarán como dispositivos XInput y DirectInput, pero no se deben controlar a través de DirectInput.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="ea3f4-135">Deberá determinar cuáles de los dispositivos DirectInput son dispositivos heredados y cuáles son dispositivos XInput y quitarlos de la enumeración de dispositivos DirectInput.</span><span class="sxs-lookup"><span data-stu-id="ea3f4-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="ea3f4-136">Para ello, inserte este código en la devolución de llamada de enumeración DirectInput:</span><span class="sxs-lookup"><span data-stu-id="ea3f4-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
        }
    }

LCleanup:
    VariantClear(&var);
    
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> <span data-ttu-id="ea3f4-137">Hay una versión ligeramente mejorada de este código en el ejemplo heredado de DirectInput [Qr.](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick)</span><span class="sxs-lookup"><span data-stu-id="ea3f4-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea3f4-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea3f4-138">Related topics</span></span>

[<span data-ttu-id="ea3f4-139">Tareas iniciales con XInput</span><span class="sxs-lookup"><span data-stu-id="ea3f4-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="ea3f4-140">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="ea3f4-140">Programming Reference</span></span>](programming-reference.md)
