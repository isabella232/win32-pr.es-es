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
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="8aa78-103">Cambios de versión del sistema operativo en Windows 8.1 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8aa78-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="8aa78-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="8aa78-104">Platforms</span></span>

<span data-ttu-id="8aa78-105">**Clientes-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8aa78-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="8aa78-106">**Servidores:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8aa78-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="8aa78-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8aa78-107">Description</span></span>

<span data-ttu-id="8aa78-108">Hemos realizado algunos cambios importantes en el funcionamiento de las API de GetVersion (ex) en Windows 8.1 debido a comportamientos de cliente no deseados que resultan de la forma en que se han usado las API GetVersion (ex) en el pasado.</span><span class="sxs-lookup"><span data-stu-id="8aa78-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="8aa78-109">En versiones anteriores de Windows, la llamada a las API GetVersion (ex) devolvería la versión real del sistema operativo (SO), a menos que una corrección de compatibilidad de la aplicación hubiera mitigado el proceso para darle una versión diferente.</span><span class="sxs-lookup"><span data-stu-id="8aa78-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="8aa78-110">Esto se realizó de forma provisional y estaba relativamente incompleto en cuanto al número de procesos que Microsoft podría razonablemente correcciones de compatibilidad (shim) en una versión.</span><span class="sxs-lookup"><span data-stu-id="8aa78-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="8aa78-111">Muchas aplicaciones se exponían a través de las grietas porque no obtuvieron corregido debido a comprobaciones de versión mal diseñadas.</span><span class="sxs-lookup"><span data-stu-id="8aa78-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="8aa78-112">El número uno de los motivos para realizar una comprobación de la versión es advertir al usuario de que la aplicación debe ejecutarse en una versión más reciente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8aa78-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="8aa78-113">Sin embargo, debido a las comprobaciones incorrectas, las aplicaciones a menudo avisaban incorrectamente de que debían ejecutarse en Windows XP o posterior, que, por supuesto, es el sistema operativo más reciente.</span><span class="sxs-lookup"><span data-stu-id="8aa78-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="8aa78-114">Con mayor frecuencia que no, el sistema operativo más reciente ejecutaría la aplicación sin ningún problema si no se tratara de estas comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="8aa78-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8aa78-115">Manifestación</span><span class="sxs-lookup"><span data-stu-id="8aa78-115">Manifestation</span></span>

<span data-ttu-id="8aa78-116">En Windows 8.1, las API GetVersion (ex) han quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="8aa78-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="8aa78-117">Esto significa que, aunque puede seguir llamando a estas funciones de API, si la aplicación no tiene como destino específicamente Windows 8.1, las funciones devolverán la versión de Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="8aa78-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="8aa78-118">Solución</span><span class="sxs-lookup"><span data-stu-id="8aa78-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="8aa78-119">Agregar un manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="8aa78-119">Adding an app manifest</span></span>

<span data-ttu-id="8aa78-120">Para que la aplicación tenga como destino Windows 8.1, debe incluir un [manifiesto de aplicación (ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8aa78-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="8aa78-121">A continuación, en la sección de [ **&lt; compatibilidad &gt;**](../SbsCs/application-manifests.md#compatibility) del manifiesto, deberá agregar un elemento **&lt; Supported &gt;** para cada versión de Windows que quiera declarar que admita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8aa78-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="8aa78-122">En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que es compatible con todas las versiones de Windows de Windows Vista para Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="8aa78-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

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

<span data-ttu-id="8aa78-123">La línea anterior marcada `* ADD THIS LINE *` muestra cómo dirigirse a la aplicación con precisión para Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8aa78-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="8aa78-124">La declaración de compatibilidad para Windows 8.1 en el manifiesto de la aplicación no tendrá ningún efecto cuando se ejecute la aplicación en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="8aa78-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="8aa78-125">Usar VersionHelpers en lugar de GetVersion (ex)</span><span class="sxs-lookup"><span data-stu-id="8aa78-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="8aa78-126">Windows 8.1 introduce nuevas funciones de la API de reemplazo para GetVersion (ex), conocido como VersionHelpers.</span><span class="sxs-lookup"><span data-stu-id="8aa78-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="8aa78-127">Son muy fáciles de usar; lo único que tiene que hacer es `#include <VersionHelpers.h>` .</span><span class="sxs-lookup"><span data-stu-id="8aa78-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="8aa78-128">Las funciones insertadas disponibles en el archivo de encabezado VersionHelpers. h permiten que el código pregunte si el sistema operativo es una versión determinada de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="8aa78-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="8aa78-129">**Ejemplo** de Por ejemplo, si la aplicación requiere Windows 8 o una versión posterior, use la siguiente prueba:</span><span class="sxs-lookup"><span data-stu-id="8aa78-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="8aa78-130">Las funciones de API de VersionHelper disponibles son:</span><span class="sxs-lookup"><span data-stu-id="8aa78-130">The available VersionHelper API functions are:</span></span>

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

<span data-ttu-id="8aa78-131">Devolverán TRUE o FALSE en función de la pregunta que esté preguntando y solo necesitará definir el sistema operativo de nivel mínimo que admita.</span><span class="sxs-lookup"><span data-stu-id="8aa78-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="8aa78-132">Recursos</span><span class="sxs-lookup"><span data-stu-id="8aa78-132">Resources</span></span>

-   [<span data-ttu-id="8aa78-133">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8aa78-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="8aa78-134">[Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8aa78-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="8aa78-135">API de VersionHelpers</span><span class="sxs-lookup"><span data-stu-id="8aa78-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)