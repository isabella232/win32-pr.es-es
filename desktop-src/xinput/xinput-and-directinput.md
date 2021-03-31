---
title: XInput y DirectInput
description: XInput es una API que permite que las aplicaciones reciban datos de la controladora Xbox para Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcdbc31a66d4928b52ae5d097cab0e877f6f078
ms.sourcegitcommit: 48d4947b16f1ed1eaf6fae2b75954b736dd25450
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/29/2020
ms.locfileid: "103794176"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="62e6a-103">XInput y DirectInput</span><span class="sxs-lookup"><span data-stu-id="62e6a-103">XInput and DirectInput</span></span>

<span data-ttu-id="62e6a-104">XInput es una API que permite que las aplicaciones reciban datos de la controladora Xbox para Windows.</span><span class="sxs-lookup"><span data-stu-id="62e6a-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="62e6a-105">En este documento se describen las diferencias entre las implementaciones de XInput y de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controlador de Xbox y cómo puede admitir dispositivos XInput y dispositivos de DirectInput heredados al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="62e6a-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="62e6a-106">No se recomienda el uso de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredado y DirectInput no está disponible para las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="62e6a-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="62e6a-107">El nuevo estándar: XInput</span><span class="sxs-lookup"><span data-stu-id="62e6a-107">The New Standard: XInput</span></span>

<span data-ttu-id="62e6a-108">XInput ya está disponible para el desarrollo de juegos.</span><span class="sxs-lookup"><span data-stu-id="62e6a-108">XInput is now available for game development.</span></span> <span data-ttu-id="62e6a-109">Este es el nuevo estándar de entrada para Xbox y Windows.</span><span class="sxs-lookup"><span data-stu-id="62e6a-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="62e6a-110">Las API están disponibles a través del SDK de DirectX y el controlador está disponible a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="62e6a-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="62e6a-111">Hay varias ventajas en el uso de XInput en [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="62e6a-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="62e6a-112">XInput es más fácil de usar y requiere menos configuración que [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62e6a-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="62e6a-113">Tanto la programación de Xbox como la de Windows usarán los mismos conjuntos de API principales, lo que permite que la programación traduzca mucho más fácilmente</span><span class="sxs-lookup"><span data-stu-id="62e6a-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="62e6a-114">Habrá una gran base instalada de controladores de Xbox</span><span class="sxs-lookup"><span data-stu-id="62e6a-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="62e6a-115">Los dispositivos XInput (es decir, los controladores de Xbox) solo tendrán la funcionalidad de vibración al usar las API de XInput</span><span class="sxs-lookup"><span data-stu-id="62e6a-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="62e6a-116">Los controladores futuros que se publiquen para la consola Xbox (es decir, las ruedas de gobierno) también funcionarán en Windows</span><span class="sxs-lookup"><span data-stu-id="62e6a-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="62e6a-117">Usar el controlador Xbox con DirectInput</span><span class="sxs-lookup"><span data-stu-id="62e6a-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="62e6a-118">La controladora Xbox está correctamente enumerada en [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))y se puede usar con DirectInputAPIs.</span><span class="sxs-lookup"><span data-stu-id="62e6a-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="62e6a-119">Sin embargo, algunas funciones que proporciona XInput no se mostrarán en la implementación de DirectInput:</span><span class="sxs-lookup"><span data-stu-id="62e6a-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="62e6a-120">Los botones de desencadenador izquierdo y derecho actuarán como un solo botón, no independientemente</span><span class="sxs-lookup"><span data-stu-id="62e6a-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="62e6a-121">Los efectos de vibración no estarán disponibles</span><span class="sxs-lookup"><span data-stu-id="62e6a-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="62e6a-122">Las consultas de dispositivos con auriculares no estarán disponibles</span><span class="sxs-lookup"><span data-stu-id="62e6a-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="62e6a-123">La combinación de los desencadenadores izquierdo y derecho de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) es por diseño.</span><span class="sxs-lookup"><span data-stu-id="62e6a-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="62e6a-124">Los juegos siempre suponen que los ejes del dispositivo DirectInput están centrados cuando no hay ninguna interacción del usuario con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62e6a-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="62e6a-125">Sin embargo, el controlador Xbox se diseñó para registrar el valor mínimo, no el centro, cuando no se mantienen los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="62e6a-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="62e6a-126">Por lo tanto, los juegos más antiguos suponen la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="62e6a-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="62e6a-127">La solución era combinar los desencadenadores, establecer un desencadenador en una dirección positiva y otro en una dirección negativa, por lo que ninguna interacción del usuario es [indicativa de que](/previous-versions/windows/desktop/ee416842(v=vs.85)) el "control" esté en el centro.</span><span class="sxs-lookup"><span data-stu-id="62e6a-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="62e6a-128">Para probar los valores del desencadenador por separado, debe usar XInput.</span><span class="sxs-lookup"><span data-stu-id="62e6a-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="62e6a-129">XInput y DirectInput en paralelo</span><span class="sxs-lookup"><span data-stu-id="62e6a-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="62e6a-130">Al admitir XInput únicamente, el juego no funcionará con los dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredados.</span><span class="sxs-lookup"><span data-stu-id="62e6a-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="62e6a-131">XInput no reconocerá estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="62e6a-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="62e6a-132">Si desea que el juego admita dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredados, puede usar DirectInput y XInput en paralelo.</span><span class="sxs-lookup"><span data-stu-id="62e6a-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="62e6a-133">Al enumerar los dispositivos de DirectInput, todos los dispositivos de DirectInput se enumerarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="62e6a-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="62e6a-134">Todos los dispositivos XInput aparecerán como dispositivos XInput y DirectInput, pero no deben controlarse a través de DirectInput.</span><span class="sxs-lookup"><span data-stu-id="62e6a-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="62e6a-135">Tendrá que determinar qué dispositivos de DirectInput son dispositivos heredados y cuáles son los dispositivos XInput y quitarlos de la enumeración de los dispositivos de DirectInput.</span><span class="sxs-lookup"><span data-stu-id="62e6a-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="62e6a-136">Para ello, inserte este código en su devolución de llamada de enumeración de DirectInput:</span><span class="sxs-lookup"><span data-stu-id="62e6a-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>
#include <wmsstd.h>

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator  = NULL;
    IEnumWbemClassObject*   pEnumDevices   = NULL;
    IWbemClassObject*       pDevices[20]   = {0};
    IWbemServices*          pIWbemServices = NULL;
    BSTR                    bstrNamespace  = NULL;
    BSTR                    bstrDeviceID   = NULL;
    BSTR                    bstrClassName  = NULL;
    DWORD                   uReturned      = 0;
    bool                    bIsXinputDevice= false;
    UINT                    iDevice        = 0;
    VARIANT                 var;
    HRESULT                 hr;

    // CoInit if needed
    hr = CoInitialize(NULL);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance( __uuidof(WbemLocator),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(IWbemLocator),
                           (LPVOID*) &pIWbemLocator);
    if( FAILED(hr) || pIWbemLocator == NULL )
        goto LCleanup;

    bstrNamespace = SysAllocString( L"\\\\.\\root\\cimv2" );if( bstrNamespace == NULL ) goto LCleanup;        
    bstrClassName = SysAllocString( L"Win32_PNPEntity" );   if( bstrClassName == NULL ) goto LCleanup;        
    bstrDeviceID  = SysAllocString( L"DeviceID" );          if( bstrDeviceID == NULL )  goto LCleanup;        
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer( bstrNamespace, NULL, NULL, 0L, 
                                       0L, NULL, NULL, &pIWbemServices );
    if( FAILED(hr) || pIWbemServices == NULL )
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    CoSetProxyBlanket( pIWbemServices, RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, NULL, 
                       RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE );                    

    hr = pIWbemServices->CreateInstanceEnum( bstrClassName, 0, NULL, &pEnumDevices ); 
    if( FAILED(hr) || pEnumDevices == NULL )
        goto LCleanup;

    // Loop over all devices
    for( ;; )
    {
        // Get 20 at a time
        hr = pEnumDevices->Next( 10000, 20, pDevices, &uReturned );
        if( FAILED(hr) )
            goto LCleanup;
        if( uReturned == 0 )
            break;

        for( iDevice=0; iDevice<uReturned; iDevice++ )
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get( bstrDeviceID, 0L, &var, NULL, NULL );
            if( SUCCEEDED( hr ) && var.vt == VT_BSTR && var.bstrVal != NULL )
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                    // This information can not be found from DirectInput 
                if( wcsstr( var.bstrVal, L"IG_" ) )
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr( var.bstrVal, L"VID_" );
                    if( strVid && swscanf( strVid, L"VID_%4X", &dwVid ) != 1 )
                        dwVid = 0;
                    WCHAR* strPid = wcsstr( var.bstrVal, L"PID_" );
                    if( strPid && swscanf( strPid, L"PID_%4X", &dwPid ) != 1 )
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG( dwVid, dwPid );
                    if( dwVidPid == pGuidProductFromDirectInput->Data1 )
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE( pDevices[iDevice] );
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
    for( iDevice=0; iDevice<20; iDevice++ )
        SAFE_RELEASE( pDevices[iDevice] );
    SAFE_RELEASE( pEnumDevices );
    SAFE_RELEASE( pIWbemLocator );
    SAFE_RELEASE( pIWbemServices );

    if( bCleanupCOM )
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
    HRESULT hr;

    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

## <a name="related-topics"></a><span data-ttu-id="62e6a-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62e6a-137">Related topics</span></span>

[<span data-ttu-id="62e6a-138">Introducción con XInput</span><span class="sxs-lookup"><span data-stu-id="62e6a-138">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="62e6a-139">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="62e6a-139">Programming Reference</span></span>](programming-reference.md)
