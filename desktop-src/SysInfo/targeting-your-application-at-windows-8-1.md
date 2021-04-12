---
description: En Windows 8.1 y Windows 10, las funciones GetVersion y GetVersionEx están desusadas.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Destino de la aplicación para Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361290"
---
# <a name="targeting-your-application-for-windows"></a><span data-ttu-id="58c71-103">Destino de la aplicación para Windows</span><span class="sxs-lookup"><span data-stu-id="58c71-103">Targeting your application for Windows</span></span>

<span data-ttu-id="58c71-104">En Windows 8.1 y Windows 10, las funciones [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) y [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) están desusadas.</span><span class="sxs-lookup"><span data-stu-id="58c71-104">In Windows 8.1 and Windows 10, the [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) and [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) functions have been deprecated.</span></span> <span data-ttu-id="58c71-105">En Windows 10, la función [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) también está en desuso.</span><span class="sxs-lookup"><span data-stu-id="58c71-105">In Windows 10, the [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) function has also been deprecated.</span></span> <span data-ttu-id="58c71-106">Aunque todavía puede llamar a las funciones desusadas, si la aplicación no tiene como destino específicamente Windows 8.1 o Windows 10, las funciones devolverán la versión de Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="58c71-106">While you can still call the deprecated functions, if your application does not specifically target Windows 8.1 or Windows 10, the functions will return the Windows 8 version (6.2).</span></span>

> [!Note]  
> <span data-ttu-id="58c71-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)y las [funciones auxiliares](version-helper-apis.md) de la versión son solo para aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="58c71-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa), and the [Version Helper functions](version-helper-apis.md) are for desktop apps only.</span></span> <span data-ttu-id="58c71-108">Las aplicaciones universales de Windows pueden usar la propiedad [**AnalyticsInfo. versionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) para la telemetría y los registros de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="58c71-108">Universal Windows apps can use the [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) property for telemetry and diagnostic logs.</span></span>

<span data-ttu-id="58c71-109">Para que la aplicación tenga como destino Windows 8.1 o Windows 10, deberá incluir un [manifiesto de aplicación (ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="58c71-109">In order for your app to target Windows 8.1 or Windows 10, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="58c71-110">A continuación, en la sección de [ **&lt; compatibilidad &gt;**](../SbsCs/application-manifests.md#compatibility) del manifiesto, deberá agregar un elemento **&lt; Supported &gt;** para cada versión de Windows que quiera declarar que admita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="58c71-110">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="58c71-111">En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que admite todas las versiones de Windows de Windows Vista a Windows 10:</span><span class="sxs-lookup"><span data-stu-id="58c71-111">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

<span data-ttu-id="58c71-112">La declaración de compatibilidad para Windows 8.1 o Windows 10 en el manifiesto de la aplicación no tendrá ningún efecto cuando se ejecute la aplicación en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="58c71-112">Declaring support for Windows 8.1 or Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

<span data-ttu-id="58c71-113">El manifiesto de aplicación anterior también incluye una [sección **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), que especifica el modo en que el sistema debe tratarlo con respecto al control de cuentas de [usuario (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span><span class="sxs-lookup"><span data-stu-id="58c71-113">The above app manifest also includes a [**&lt;trustInfo&gt;** section](/previous-versions/bb756929(v=msdn.10)), which specifies how the system should treat it with respect to [User Account Control (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span></span> <span data-ttu-id="58c71-114">Agregar **trustInfo** no es esencial, pero se recomienda encarecidamente, incluso cuando la aplicación no necesite ningún comportamiento concreto relacionado con UAC.</span><span class="sxs-lookup"><span data-stu-id="58c71-114">Adding **trustInfo** isn't essential, but it is highly recommended, even when your app doesn't need any particular UAC-related behavior.</span></span> <span data-ttu-id="58c71-115">En concreto, si no agrega **trustInfo** , las versiones x86 de 32 bits de la aplicación estarán sujetas a la [virtualización de archivos de UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), lo que permite que las escrituras en carpetas con privilegios de administrador, como las carpetas del sistema de Windows, se realicen correctamente cuando se produzcan errores, pero se redirigirán a una carpeta "VirtualStore" específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="58c71-115">In particular, if you don't add **trustInfo** at all, then 32-bit x86 versions of your app will be subject to [UAC file virtualization](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), which allows writes to administrator-privileged folders like the Windows system folders to succeed when they would otherwise fail, but redirects them to a user-specific "VirtualStore" folder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58c71-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58c71-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58c71-117">Obtener la versión del sistema</span><span class="sxs-lookup"><span data-stu-id="58c71-117">Getting the system version</span></span>](getting-the-system-version.md)
</dt> <dt>

[<span data-ttu-id="58c71-118">Funciones auxiliares de versión</span><span class="sxs-lookup"><span data-stu-id="58c71-118">Version Helper functions</span></span>](version-helper-apis.md)
</dt> <dt>

[<span data-ttu-id="58c71-119">OSVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="58c71-119">OSVERSIONINFO</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[<span data-ttu-id="58c71-120">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="58c71-120">OSVERSIONINFOEX</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
