---
description: En Windows 8.1 y Windows 10, las funciones GetVersion y GetVersionEx han quedado en desuso.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Destino de la aplicación para Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e045dff2f46501c4715e2ffebe484dfeadb3aa9f276d79c7e7c1afdbec6ba7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763116"
---
# <a name="targeting-your-application-for-windows"></a>Destino de la aplicación para Windows

En Windows 8.1 y Windows 10, las [**funciones GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) y [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) han quedado en desuso. En Windows 10, la [**función VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) también ha quedado en desuso. Aunque todavía puede llamar a las funciones en desuso, si la aplicación no tiene como destino específica Windows 8.1 o Windows 10, las funciones devolverán la versión Windows 8 (6.2).

> [!Note]  
> [**GetVersion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [**GetVersionEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)y las funciones del asistente [de versiones](version-helper-apis.md) son solo para aplicaciones de escritorio. Las aplicaciones Windows universales pueden usar la [**propiedad AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) para los registros de telemetría y diagnóstico.

Para que la aplicación tenga como destino Windows 8.1 o Windows 10, deberá incluir un manifiesto de aplicación [(ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación. A continuación, [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) en la sección de compatibilidad del manifiesto, deberá agregar un elemento **&lt; supportedOS &gt;** para cada versión Windows que quiera declarar que admite la aplicación.

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

Declarar la compatibilidad con Windows 8.1 o Windows 10 en el manifiesto de aplicación no tendrá ningún efecto al ejecutar la aplicación en sistemas operativos anteriores.

El manifiesto de aplicación anterior también incluye una [ **&lt; sección trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), que especifica cómo el sistema debe tratarlo con respecto al Control de cuentas de usuario [(UAC).](/windows/security/identity-protection/user-account-control/how-user-account-control-works) Agregar **trustInfo** no es esencial, pero es muy recomendable, incluso cuando la aplicación no necesita ningún comportamiento relacionado con UAC concreto. En concreto, si no agrega **trustInfo** en absoluto, las versiones x86 de 32 bits de la aplicación estarán sujetas a la virtualización de archivos [UAC,](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization)que permite que las escrituras en carpetas con privilegios de administrador, como las carpetas del sistema de Windows, se realizaran correctamente cuando de lo contrario se produciría un error, pero las redirige a una carpeta "VirtualStore" específica del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtención de la versión del sistema](getting-the-system-version.md)
</dt> <dt>

[Funciones del asistente de versiones](version-helper-apis.md)
</dt> <dt>

[OSVERSIONINFO](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
