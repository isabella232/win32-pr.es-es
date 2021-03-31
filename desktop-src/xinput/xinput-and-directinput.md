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
# <a name="xinput-and-directinput"></a>XInput y DirectInput

XInput es una API que permite que las aplicaciones reciban datos de la controladora Xbox para Windows. En este documento se describen las diferencias entre las implementaciones de XInput y de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controlador de Xbox y cómo puede admitir dispositivos XInput y dispositivos de DirectInput heredados al mismo tiempo.

> [!Note]  
> No se recomienda el uso de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredado y DirectInput no está disponible para las aplicaciones de la tienda Windows.

## <a name="the-new-standard-xinput"></a>El nuevo estándar: XInput

XInput ya está disponible para el desarrollo de juegos. Este es el nuevo estándar de entrada para Xbox y Windows. Las API están disponibles a través del SDK de DirectX y el controlador está disponible a través de Windows Update.

Hay varias ventajas en el uso de XInput en [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):

-   XInput es más fácil de usar y requiere menos configuración que [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   Tanto la programación de Xbox como la de Windows usarán los mismos conjuntos de API principales, lo que permite que la programación traduzca mucho más fácilmente
-   Habrá una gran base instalada de controladores de Xbox
-   Los dispositivos XInput (es decir, los controladores de Xbox) solo tendrán la funcionalidad de vibración al usar las API de XInput
-   Los controladores futuros que se publiquen para la consola Xbox (es decir, las ruedas de gobierno) también funcionarán en Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Usar el controlador Xbox con DirectInput

La controladora Xbox está correctamente enumerada en [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))y se puede usar con DirectInputAPIs. Sin embargo, algunas funciones que proporciona XInput no se mostrarán en la implementación de DirectInput:

-   Los botones de desencadenador izquierdo y derecho actuarán como un solo botón, no independientemente
-   Los efectos de vibración no estarán disponibles
-   Las consultas de dispositivos con auriculares no estarán disponibles

La combinación de los desencadenadores izquierdo y derecho de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) es por diseño. Los juegos siempre suponen que los ejes del dispositivo DirectInput están centrados cuando no hay ninguna interacción del usuario con el dispositivo. Sin embargo, el controlador Xbox se diseñó para registrar el valor mínimo, no el centro, cuando no se mantienen los desencadenadores. Por lo tanto, los juegos más antiguos suponen la interacción del usuario.

La solución era combinar los desencadenadores, establecer un desencadenador en una dirección positiva y otro en una dirección negativa, por lo que ninguna interacción del usuario es [indicativa de que](/previous-versions/windows/desktop/ee416842(v=vs.85)) el "control" esté en el centro.

Para probar los valores del desencadenador por separado, debe usar XInput.

## <a name="xinput-and-directinput-side-by-side"></a>XInput y DirectInput en paralelo

Al admitir XInput únicamente, el juego no funcionará con los dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredados. XInput no reconocerá estos dispositivos.

Si desea que el juego admita dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredados, puede usar DirectInput y XInput en paralelo. Al enumerar los dispositivos de DirectInput, todos los dispositivos de DirectInput se enumerarán correctamente. Todos los dispositivos XInput aparecerán como dispositivos XInput y DirectInput, pero no deben controlarse a través de DirectInput. Tendrá que determinar qué dispositivos de DirectInput son dispositivos heredados y cuáles son los dispositivos XInput y quitarlos de la enumeración de los dispositivos de DirectInput.

Para ello, inserte este código en su devolución de llamada de enumeración de DirectInput:

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

## <a name="related-topics"></a>Temas relacionados

[Introducción con XInput](getting-started-with-xinput.md)

[Referencia de programación](programming-reference.md)
