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
# <a name="targeting-your-application-for-windows"></a>Destino de la aplicación para Windows

En Windows 8.1 y Windows 10, las funciones [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) y [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) están desusadas. En Windows 10, la función [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) también está en desuso. Aunque todavía puede llamar a las funciones desusadas, si la aplicación no tiene como destino específicamente Windows 8.1 o Windows 10, las funciones devolverán la versión de Windows 8 (6,2).

> [!Note]  
> [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)y las [funciones auxiliares](version-helper-apis.md) de la versión son solo para aplicaciones de escritorio. Las aplicaciones universales de Windows pueden usar la propiedad [**AnalyticsInfo. versionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) para la telemetría y los registros de diagnóstico.

Para que la aplicación tenga como destino Windows 8.1 o Windows 10, deberá incluir un [manifiesto de aplicación (ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación. A continuación, en la sección de [ **&lt; compatibilidad &gt;**](../SbsCs/application-manifests.md#compatibility) del manifiesto, deberá agregar un elemento **&lt; Supported &gt;** para cada versión de Windows que quiera declarar que admita la aplicación.

En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que admite todas las versiones de Windows de Windows Vista a Windows 10:

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

La declaración de compatibilidad para Windows 8.1 o Windows 10 en el manifiesto de la aplicación no tendrá ningún efecto cuando se ejecute la aplicación en sistemas operativos anteriores.

El manifiesto de aplicación anterior también incluye una [sección **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), que especifica el modo en que el sistema debe tratarlo con respecto al control de cuentas de [usuario (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works). Agregar **trustInfo** no es esencial, pero se recomienda encarecidamente, incluso cuando la aplicación no necesite ningún comportamiento concreto relacionado con UAC. En concreto, si no agrega **trustInfo** , las versiones x86 de 32 bits de la aplicación estarán sujetas a la [virtualización de archivos de UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), lo que permite que las escrituras en carpetas con privilegios de administrador, como las carpetas del sistema de Windows, se realicen correctamente cuando se produzcan errores, pero se redirigirán a una carpeta "VirtualStore" específica del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener la versión del sistema](getting-the-system-version.md)
</dt> <dt>

[Funciones auxiliares de versión](version-helper-apis.md)
</dt> <dt>

[OSVERSIONINFO](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
