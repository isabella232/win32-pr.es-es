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
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="da53d-103">Audiencia del desarrollador y código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="da53d-103">Developer audience, and sample code</span></span>

<span data-ttu-id="da53d-104">La interfaz de examen antimalware está diseñada para que la usen dos grupos de desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="da53d-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="da53d-105">Desarrolladores de aplicaciones que desean hacer solicitudes a productos antimalware desde sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="da53d-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="da53d-106">Creadores de productos antimalware de terceros que desean que sus productos ofrezcan las mejores características a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="da53d-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="da53d-107">Desarrolladores de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="da53d-107">Application developers</span></span>

<span data-ttu-id="da53d-108">AMSI está diseñado específicamente para combatir el "malware con archivos".</span><span class="sxs-lookup"><span data-stu-id="da53d-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="da53d-109">Entre los tipos de aplicaciones que pueden aprovechar óptimamente la tecnología AMSI se incluyen motores de scripts, aplicaciones que necesitan que se examinen los búferes de memoria antes de usarlos y aplicaciones que procesan archivos que pueden contener código ejecutable que no es de PE (como macros de Microsoft Word y Excel, o documentos PDF).</span><span class="sxs-lookup"><span data-stu-id="da53d-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="da53d-110">Sin embargo, la utilidad de la tecnología AMSI no se limita a los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="da53d-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="da53d-111">Hay dos maneras de interactuar con AMSI en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da53d-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="da53d-112">Mediante el uso de las API de Win32 de AMSI.</span><span class="sxs-lookup"><span data-stu-id="da53d-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="da53d-113">Consulte [funciones de la interfaz de examen antimalware (Amsi)](/windows/desktop/amsi/antimalware-scan-interface-functions).</span><span class="sxs-lookup"><span data-stu-id="da53d-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="da53d-114">Mediante el uso de las interfaces COM AMSI.</span><span class="sxs-lookup"><span data-stu-id="da53d-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="da53d-115">Consulte la [interfaz **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span><span class="sxs-lookup"><span data-stu-id="da53d-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="da53d-116">Para ver el código de ejemplo que muestra cómo consumir AMSI dentro de la aplicación COM, consulte la aplicación de ejemplo de la [interfaz IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span><span class="sxs-lookup"><span data-stu-id="da53d-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="da53d-117">Creadores de productos antimalware de terceros</span><span class="sxs-lookup"><span data-stu-id="da53d-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="da53d-118">Como creador de los productos antimalware, puede optar por crear y registrar su propio servidor COM en proceso (un archivo DLL) para que funcione como un proveedor de AMSI.</span><span class="sxs-lookup"><span data-stu-id="da53d-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="da53d-119">Ese proveedor AMSI debe implementar la [interfaz **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)y debe ejecutarse en proceso.</span><span class="sxs-lookup"><span data-stu-id="da53d-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="da53d-120">Tenga en cuenta que, después de Windows 10, versión 1709 (actualización de 2017 creadores), es posible que la DLL del proveedor de AMSI no funcione si depende de otros archivos dll en su ruta de acceso que se van a cargar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="da53d-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="da53d-121">Para evitar el secuestro de archivos DLL, se recomienda que el archivo DLL del proveedor cargue sus dependencias explícitamente (con una ruta de acceso completa) mediante llamadas [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) seguras o equivalentes.</span><span class="sxs-lookup"><span data-stu-id="da53d-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="da53d-122">Se recomienda esto en lugar de confiar en el comportamiento de la búsqueda **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="da53d-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="da53d-123">En la sección siguiente se muestra cómo registrar el proveedor de AMSI.</span><span class="sxs-lookup"><span data-stu-id="da53d-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="da53d-124">Para ver el código de ejemplo completo que muestra cómo crear su propio archivo DLL de proveedor de AMSI, consulte la aplicación de ejemplo de la [interfaz IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span><span class="sxs-lookup"><span data-stu-id="da53d-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="da53d-125">Registro de la DLL de proveedor con AMSI</span><span class="sxs-lookup"><span data-stu-id="da53d-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="da53d-126">Para empezar, debe asegurarse de que existen estas claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="da53d-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="da53d-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span><span class="sxs-lookup"><span data-stu-id="da53d-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="da53d-128">HKLM\SOFTWARE\Classes\CLSID</span><span class="sxs-lookup"><span data-stu-id="da53d-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="da53d-129">Un proveedor de AMSI es un servidor COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="da53d-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="da53d-130">Por lo tanto, debe registrarse con COM.</span><span class="sxs-lookup"><span data-stu-id="da53d-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="da53d-131">Las clases COM están registradas en `HKLM\SOFTWARE\Classes\CLSID` .</span><span class="sxs-lookup"><span data-stu-id="da53d-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="da53d-132">En el código siguiente se muestra cómo registrar un proveedor de AMSI, cuyo GUID (en este ejemplo) se asumirá que es `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .</span><span class="sxs-lookup"><span data-stu-id="da53d-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

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

<span data-ttu-id="da53d-133">Si el archivo DLL implementa la [función DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), como hace el ejemplo anterior, puede registrarlo mediante el ejecutable proporcionado por Windows `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="da53d-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="da53d-134">Desde un símbolo del sistema con privilegios elevados, emita un comando con este formato.</span><span class="sxs-lookup"><span data-stu-id="da53d-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="da53d-135">En este ejemplo, el comando crea las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="da53d-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="da53d-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="da53d-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="da53d-137">&nbsp;&nbsp;&nbsp;&nbsp;**Predeterminada    REG_SZ implementación del proveedor de AMSI de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="da53d-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="da53d-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="da53d-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="da53d-139">&nbsp;&nbsp;&nbsp;&nbsp;**Predeterminada    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="da53d-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="da53d-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ ambos**</span><span class="sxs-lookup"><span data-stu-id="da53d-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="da53d-141">Además del registro COM normal, también debe inscribir el proveedor con AMSI.</span><span class="sxs-lookup"><span data-stu-id="da53d-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="da53d-142">Para ello, agregue una entrada a la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="da53d-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="da53d-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span><span class="sxs-lookup"><span data-stu-id="da53d-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="da53d-144">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="da53d-144">For example,</span></span>

<span data-ttu-id="da53d-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="da53d-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>
