---
title: Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2
description: Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882695"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8.1

**Servidores:** Windows Server 2012 R2

## <a name="description"></a>Descripción

Hemos realizado algunos cambios significativos en el modo en que las API de GetVersion(Ex) funcionan en Windows 8.1 debido a comportamientos no deseados de los clientes resultantes de cómo se han usado las API de GetVersion(Ex) en el pasado.

En versiones anteriores de Windows, llamar a las API GetVersion(Ex) devolvería la versión real del sistema operativo (SO), a menos que el proceso se hubiera mitigado mediante una corrección de compatibilidad de aplicación para darle una versión diferente. Esto se hizo de forma provisional y estaba relativamente incompleto en cuanto al número de procesos que Microsoft podría correcciones razonablemente de compatibilidad (shim) en una versión. Muchas aplicaciones han pasado por las fisuras porque no se han recortado debido a comprobaciones de versiones mal diseñadas.

El motivo número uno para realizar una comprobación de versión es advertir al usuario de que la aplicación debe ejecutarse en una versión más reciente del sistema operativo. Sin embargo, debido a comprobaciones deficientes, las aplicaciones a menudo advierten incorrectamente que deben ejecutarse en Windows XP o posterior, que por supuesto es el sistema operativo más reciente. Con más frecuencia que no, el sistema operativo más reciente ejecutaría la aplicación sin problemas si no fuera por estas comprobaciones.

## <a name="manifestation"></a>Manifestación

En Windows 8.1, las API GetVersion(Ex) han quedado en desuso. Esto significa que, aunque todavía puede llamar a estas funciones de API, si la aplicación no tiene como destino específica Windows 8.1, las funciones devolverán la versión Windows 8 (6.2).

## <a name="solution"></a>Solución

### <a name="adding-an-app-manifest"></a>Adición de un manifiesto de aplicación

Para que la aplicación tenga como destino Windows 8.1, deberá incluir un manifiesto de aplicación [(ejecutable)](/windows/compatibility/application-executable-manifest) para el archivo ejecutable de la aplicación. A continuación, [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) en la sección de compatibilidad del manifiesto, deberá agregar un elemento **&lt; supportedOS &gt;** para cada versión Windows que quiera declarar que admite la aplicación.

En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que admite todas las versiones de Windows de Windows Vista a Windows 8.1:

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
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

La línea anterior marcada `* ADD THIS LINE *` muestra cómo dirigirse con precisión a la aplicación para Windows 8.1.

Declarar la compatibilidad con Windows 8.1 en el manifiesto de aplicación no tendrá ningún efecto al ejecutar la aplicación en sistemas operativos anteriores.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Usar VersionHelpers en lugar de GetVersion(Ex)

Windows 8.1 nuevas funciones de API de reemplazo para GetVersion(Ex), conocidas como VersionHelpers. Son muy fáciles de usar; todo lo que tiene que hacer es `#include <VersionHelpers.h>` . Las funciones insertadas disponibles en el archivo de encabezado VersionHelpers.h permiten al código preguntar si el sistema operativo es una versión determinada de Windows o posterior.

**Ejemplo** Por ejemplo, si la aplicación requiere Windows 8 o posterior, use la siguiente prueba:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Las funciones disponibles de la API VersionHelper son:

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

Devolverán TRUE o FALSE en función de la pregunta que se haga y solo tendrá que definir el sistema operativo de nivel mínimo que admita.

## <a name="resources"></a>Recursos

-   [Compatibilidad de aplicaciones Toolkit descarga](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API versionHelpers](../sysinfo/version-helper-apis.md)