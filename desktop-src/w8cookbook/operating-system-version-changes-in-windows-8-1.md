---
title: Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2
description: Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421333"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2

## <a name="platforms"></a>Plataformas

**Clientes-** Windows 8.1

**Servidores:** Windows Server 2012 R2

## <a name="description"></a>Descripción

Hemos realizado algunos cambios importantes en el funcionamiento de las API de GetVersion (ex) en Windows 8.1 debido a comportamientos de cliente no deseados que resultan de la forma en que se han usado las API GetVersion (ex) en el pasado.

En versiones anteriores de Windows, la llamada a las API GetVersion (ex) devolvería la versión real del sistema operativo (SO), a menos que una corrección de compatibilidad de la aplicación hubiera mitigado el proceso para darle una versión diferente. Esto se realizó de forma provisional y estaba relativamente incompleto en cuanto al número de procesos que Microsoft podría razonablemente correcciones de compatibilidad (shim) en una versión. Muchas aplicaciones se exponían a través de las grietas porque no obtuvieron corregido debido a comprobaciones de versión mal diseñadas.

El número uno de los motivos para realizar una comprobación de la versión es advertir al usuario de que la aplicación debe ejecutarse en una versión más reciente del sistema operativo. Sin embargo, debido a las comprobaciones incorrectas, las aplicaciones a menudo avisaban incorrectamente de que debían ejecutarse en Windows XP o posterior, que, por supuesto, es el sistema operativo más reciente. Con mayor frecuencia que no, el sistema operativo más reciente ejecutaría la aplicación sin ningún problema si no se tratara de estas comprobaciones.

## <a name="manifestation"></a>Manifestación

En Windows 8.1, las API GetVersion (ex) han quedado en desuso. Esto significa que, aunque puede seguir llamando a estas funciones de API, si la aplicación no tiene como destino específicamente Windows 8.1, las funciones devolverán la versión de Windows 8 (6,2).

## <a name="solution"></a>Solución

### <a name="adding-an-app-manifest"></a>Agregar un manifiesto de aplicación

Para que la aplicación tenga como destino Windows 8.1, debe incluir un [manifiesto de aplicación (ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación. A continuación, en la sección de [ **&lt; compatibilidad &gt;**](../SbsCs/application-manifests.md#compatibility) del manifiesto, deberá agregar un elemento **&lt; Supported &gt;** para cada versión de Windows que quiera declarar que admita la aplicación.

En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que es compatible con todas las versiones de Windows de Windows Vista para Windows 8.1:

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

La línea anterior marcada `* ADD THIS LINE *` muestra cómo dirigirse a la aplicación con precisión para Windows 8.1.

La declaración de compatibilidad para Windows 8.1 en el manifiesto de la aplicación no tendrá ningún efecto cuando se ejecute la aplicación en sistemas operativos anteriores.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Usar VersionHelpers en lugar de GetVersion (ex)

Windows 8.1 introduce nuevas funciones de la API de reemplazo para GetVersion (ex), conocido como VersionHelpers. Son muy fáciles de usar; lo único que tiene que hacer es `#include <VersionHelpers.h>` . Las funciones insertadas disponibles en el archivo de encabezado VersionHelpers. h permiten que el código pregunte si el sistema operativo es una versión determinada de Windows o posterior.

**Ejemplo** de Por ejemplo, si la aplicación requiere Windows 8 o una versión posterior, use la siguiente prueba:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Las funciones de API de VersionHelper disponibles son:

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

Devolverán TRUE o FALSE en función de la pregunta que esté preguntando y solo necesitará definir el sistema operativo de nivel mínimo que admita.

## <a name="resources"></a>Recursos

-   [Descarga del kit de herramientas de compatibilidad de aplicaciones](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API de VersionHelpers](../sysinfo/version-helper-apis.md)