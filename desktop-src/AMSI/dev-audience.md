---
title: Audiencia del desarrollador y código de ejemplo
description: En este tema se describen los grupos de desarrolladores para los que está diseñada la interfaz de examen antimalware.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2020
ms.locfileid: "104077239"
---
# <a name="developer-audience-and-sample-code"></a>Audiencia del desarrollador y código de ejemplo

La interfaz de examen antimalware está diseñada para que la usen dos grupos de desarrolladores.

- Desarrolladores de aplicaciones que desean hacer solicitudes a productos antimalware desde sus aplicaciones.
- Creadores de productos antimalware de terceros que desean que sus productos ofrezcan las mejores características a las aplicaciones.

## <a name="application-developers"></a>Desarrolladores de aplicaciones

AMSI está diseñado específicamente para combatir el "malware con archivos". Entre los tipos de aplicaciones que pueden aprovechar óptimamente la tecnología AMSI se incluyen motores de scripts, aplicaciones que necesitan que se examinen los búferes de memoria antes de usarlos y aplicaciones que procesan archivos que pueden contener código ejecutable que no es de PE (como macros de Microsoft Word y Excel, o documentos PDF). Sin embargo, la utilidad de la tecnología AMSI no se limita a los ejemplos.

Hay dos maneras de interactuar con AMSI en la aplicación.

- Mediante el uso de las API de Win32 de AMSI. Consulte [funciones de la interfaz de examen antimalware (Amsi)](/windows/desktop/amsi/antimalware-scan-interface-functions).
- Mediante el uso de las interfaces COM AMSI. Consulte la [interfaz **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Para ver el código de ejemplo que muestra cómo consumir AMSI dentro de la aplicación COM, consulte la aplicación de ejemplo de la [interfaz IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Creadores de productos antimalware de terceros

Como creador de los productos antimalware, puede optar por crear y registrar su propio servidor COM en proceso (un archivo DLL) para que funcione como un proveedor de AMSI. Ese proveedor AMSI debe implementar la [interfaz **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)y debe ejecutarse en proceso.

Tenga en cuenta que, después de Windows 10, versión 1709 (actualización de 2017 creadores), es posible que la DLL del proveedor de AMSI no funcione si depende de otros archivos dll en su ruta de acceso que se van a cargar al mismo tiempo. Para evitar el secuestro de archivos DLL, se recomienda que el archivo DLL del proveedor cargue sus dependencias explícitamente (con una ruta de acceso completa) mediante llamadas [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) seguras o equivalentes. Se recomienda esto en lugar de confiar en el comportamiento de la búsqueda **LoadLibrary** .

En la sección siguiente se muestra cómo registrar el proveedor de AMSI. Para ver el código de ejemplo completo que muestra cómo crear su propio archivo DLL de proveedor de AMSI, consulte la aplicación de ejemplo de la [interfaz IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registro de la DLL de proveedor con AMSI

Para empezar, debe asegurarse de que existen estas claves del registro de Windows.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Un proveedor de AMSI es un servidor COM en proceso. Por lo tanto, debe registrarse con COM. Las clases COM están registradas en `HKLM\SOFTWARE\Classes\CLSID` .

En el código siguiente se muestra cómo registrar un proveedor de AMSI, cuyo GUID (en este ejemplo) se asumirá que es `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

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

Si el archivo DLL implementa la [función DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), como hace el ejemplo anterior, puede registrarlo mediante el ejecutable proporcionado por Windows `regsvr32.exe` . Desde un símbolo del sistema con privilegios elevados, emita un comando con este formato.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

En este ejemplo, el comando crea las siguientes entradas.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**Predeterminada    REG_SZ implementación del proveedor de AMSI de ejemplo**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**Predeterminada    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ ambos**

Además del registro COM normal, también debe inscribir el proveedor con AMSI. Para ello, agregue una entrada a la siguiente clave.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Por ejemplo,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
