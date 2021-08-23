---
title: Audiencia de desarrolladores y código de ejemplo
description: En este tema se describen los grupos de desarrolladores para los que está diseñada la interfaz de examen antimalware.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 4ac11c75d5714d0706bed28264f9fa1bf03432af82107826178007e2c42243c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579915"
---
# <a name="developer-audience-and-sample-code"></a>Audiencia de desarrolladores y código de ejemplo

La interfaz de examen antimalware está diseñada para su uso por dos grupos de desarrolladores.

- Desarrolladores de aplicaciones que desean realizar solicitudes a productos antimalware desde dentro de sus aplicaciones.
- Creadores de productos antimalware de terceros que desean que sus productos ofrecan las mejores características a las aplicaciones.

## <a name="application-developers"></a>Desarrolladores de aplicaciones

AMSI está diseñado en particular para combatir el "malware sin archivos". Entre los tipos de aplicación que pueden aprovechar de forma óptima la tecnología AMSI se incluyen los motores de scripts, las aplicaciones que necesitan que se digitalizarán los búferes de memoria antes de usarlos y las aplicaciones que procesan archivos que pueden contener código ejecutable no PE (como macros Microsoft Word y Excel o documentos PDF). Sin embargo, la utilidad de la tecnología AMSI no se limita a esos ejemplos.

Hay dos maneras de establecer una interfaz con AMSI en la aplicación.

- Mediante las API win32 de AMSI. Vea [Funciones de la interfaz de examen de Antimalware (AMSI).](/windows/desktop/amsi/antimalware-scan-interface-functions)
- Mediante las interfaces COM de AMSI. Vea [ **IAmsiStream interface ( Interfaz IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream)).

Para obtener código de ejemplo que muestra cómo consumir AMSI dentro de la aplicación COM, vea la aplicación de ejemplo [de interfaz IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Creadores de productos antimalware de terceros

Como creador de productos antimalware, puede optar por crear y registrar su propio servidor COM en proceso (un archivo DLL) para que funcione como proveedor de AMSI. Ese proveedor de AMSI debe implementar [ **la interfaz IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)y debe ejecutarse en proceso.

Tenga en cuenta que, después de Windows 10, versión 1709 (fall 2017 Creators' Update), es posible que el archivo DLL del proveedor amSI no funcione si depende de otros archivos DLL de su ruta de acceso que se cargarán al mismo tiempo. Para evitar el secuestro de archivos DLL, se recomienda que el archivo DLL del proveedor cargue sus dependencias explícitamente (con una ruta de acceso completa) mediante llamadas [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) seguras o equivalentes. Se recomienda esto en lugar de basarse en el comportamiento **de búsqueda loadLibrary.**

En la sección siguiente se muestra cómo registrar el proveedor de AMSI. Para obtener código de ejemplo completo que muestra cómo crear su propio archivo DLL de proveedor de AMSI, vea la aplicación de ejemplo [de interfaz IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registro del archivo DLL del proveedor con AMSI

Para empezar, debe asegurarse de que existen Windows claves del Registro.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Un proveedor AMSI es un servidor COM en proceso. Por lo tanto, debe registrarse en COM. Las clases COM se registran en `HKLM\SOFTWARE\Classes\CLSID` .

En el código siguiente se muestra cómo registrar un proveedor de AMSI, cuyo GUID (en este ejemplo) se supone que es `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

Si el archivo DLL implementa la función [DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), como en el ejemplo anterior, puede registrarla mediante el ejecutable Windows proporcionado por `regsvr32.exe` . Desde un símbolo del sistema con privilegios elevados, emita un comando de este formulario.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

En este ejemplo, el comando crea las siguientes entradas.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**(Valor predeterminado)    REG_SZ implementación del proveedor AMSI de ejemplo**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**(Valor predeterminado)    REG_EXPAND_SZ %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ ambos**

Además del registro COM normal, también debe inscribir el proveedor con AMSI. Para ello, agregue una entrada a la clave siguiente.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Por ejemplo,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
