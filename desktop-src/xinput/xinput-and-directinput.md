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
# <a name="xinput-and-directinput"></a>XInput y DirectInput

XInput es una API que permite a las aplicaciones recibir entradas del controlador de Xbox para Windows. En este documento se describen las diferencias entre las implementaciones de XInput y [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controlador de Xbox y cómo puede admitir dispositivos XInput y dispositivos DirectInput heredados al mismo tiempo.

> [!Note]  
> No se recomienda el [uso de DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredado y DirectInput no está disponible para Windows Store.

## <a name="the-new-standard-xinput"></a>El nuevo estándar: XInput

XInput ya está disponible para el desarrollo de juegos. Este es el nuevo estándar de entrada para Xbox y Windows. Las API están disponibles a través del SDK de DirectX y el controlador está disponible a través de Windows Update.

El uso de XInput sobre DirectInput tiene varias [ventajas:](/previous-versions/windows/desktop/ee416842(v=vs.85))

-   XInput es más fácil de usar y requiere menos configuración que [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   Tanto Xbox como Windows programación usarán los mismos conjuntos de API principales, lo que permite que la programación traduzca la multiplataforma mucho más fácil.
-   Habrá una gran base instalada de controladores de Xbox.
-   Los dispositivos XInput (es decir, los controladores de Xbox) solo tendrán funcionalidad de vibración cuando se usen las API XInput.
-   Los controladores futuros publicados para la consola Xbox (es decir, las ruedas de ruedas) también funcionarán en Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Uso del controlador xbox con DirectInput

El controlador de Xbox se enumera correctamente en [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))y se puede usar con directInputAPIs. Sin embargo, faltará alguna funcionalidad proporcionada por XInput en la implementación de DirectInput:

-   Los botones de desencadenador izquierdo y derecho actuarán como un botón único, no de forma independiente.
-   Los efectos de vibración no estarán disponibles
-   Las consultas de dispositivos de casco no estarán disponibles

La combinación de los desencadenadores izquierdo y derecho [en DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) es por diseño. Los juegos siempre han asumido que los ejes del dispositivo DirectInput están centrados cuando no hay ninguna interacción del usuario con el dispositivo. Sin embargo, el controlador de Xbox se diseñó para registrar el valor mínimo, no el centro, cuando no se mantienen los desencadenadores. Por lo tanto, los juegos más antiguos asumirían la interacción del usuario.

La solución era combinar los desencadenadores, estableciendo un desencadenador en una dirección positiva y el otro en una dirección negativa, por lo que ninguna interacción del usuario es indicativa a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) de que el "control" está en el centro.

Para probar los valores del desencadenador por separado, debe usar XInput.

## <a name="xinput-and-directinput-side-by-side"></a>XInput y DirectInput en paralelo

Al admitir solo XInput, el juego no funcionará con dispositivos [DirectInput heredados.](/previous-versions/windows/desktop/ee416842(v=vs.85)) XInput no reconocerá estos dispositivos.

Si quiere que el juego admita dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) heredados, puede usar DirectInput y XInput en paralelo. Al enumerar los dispositivos DirectInput, todos los dispositivos DirectInput se enumerarán correctamente. Todos los dispositivos XInput se mostrarán como dispositivos XInput y DirectInput, pero no se deben controlar a través de DirectInput. Deberá determinar cuáles de los dispositivos DirectInput son dispositivos heredados y cuáles son dispositivos XInput y quitarlos de la enumeración de dispositivos DirectInput.

Para ello, inserte este código en la devolución de llamada de enumeración DirectInput:

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

> Hay una versión ligeramente mejorada de este código en el ejemplo heredado de DirectInput [Qr.](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick)

## <a name="related-topics"></a>Temas relacionados

[Tareas iniciales con XInput](getting-started-with-xinput.md)

[Referencia de programación](programming-reference.md)
