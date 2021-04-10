---
title: Comprobación de la versión de Windows
description: La versión del sistema operativo se ha incrementado con la versión del sistema operativo Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149699"
---
# <a name="windows-version-check"></a><span data-ttu-id="52db0-103">Comprobación de la versión de Windows</span><span class="sxs-lookup"><span data-stu-id="52db0-103">Windows version check</span></span>

<span data-ttu-id="52db0-104">La versión del sistema operativo se ha incrementado con la versión del sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="52db0-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="52db0-105">Esto significa que el número de versión interno de Windows 10 también se ha cambiado a 10,0.</span><span class="sxs-lookup"><span data-stu-id="52db0-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="52db0-106">Como ya sucedió en su día, hacemos todo lo posible para mantener la compatibilidad de los dispositivos y las aplicaciones tras un cambio de versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52db0-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="52db0-107">Para la mayoría de las categorías de aplicaciones (sin ninguna dependencia de kernel), el cambio no afectará negativamente a la funcionalidad de la aplicación y las aplicaciones existentes seguirán funcionando correctamente en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="52db0-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="52db0-108">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="52db0-108">Manifestations</span></span>

<span data-ttu-id="52db0-109">La manifestación de este cambio es específica de cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="52db0-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="52db0-110">Esto significa que cualquier aplicación que compruebe específicamente la versión del sistema operativo obtendrá un número de versión superior, lo que puede ocasionar una o varias de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="52db0-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="52db0-111">Es posible que los instaladores de aplicaciones no puedan instalar la aplicación y que las aplicaciones no puedan iniciarse.</span><span class="sxs-lookup"><span data-stu-id="52db0-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="52db0-112">Las aplicaciones podrían volverse inestables o bloquearse.</span><span class="sxs-lookup"><span data-stu-id="52db0-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="52db0-113">Las aplicaciones podrían generar mensajes de error, pero seguir funcionando correctamente.</span><span class="sxs-lookup"><span data-stu-id="52db0-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="52db0-114">Algunas aplicaciones realizan una comprobación de la versión y simplemente muestran una advertencia a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="52db0-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="52db0-115">Sin embargo, hay aplicaciones que están enlazadas muy estrechamente a una comprobación de la versión (por ejemplo, en los controladores o en el modo kernel para evitar la detección).</span><span class="sxs-lookup"><span data-stu-id="52db0-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="52db0-116">En estos casos, si se encuentra una versión incorrecta, se producirá un error en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="52db0-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="52db0-117">En lugar de una comprobación de la versión, recomendamos uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="52db0-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="52db0-118">Si la aplicación depende de la funcionalidad de una API específica, asegúrate de que apuntas a la versión correcta de dicha API.</span><span class="sxs-lookup"><span data-stu-id="52db0-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="52db0-119">El número de versión de NTDDI (interfaz de controlador de dispositivo NT) solo se incrementará si cambia la funcionalidad de destino en la API.</span><span class="sxs-lookup"><span data-stu-id="52db0-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="52db0-120">Asegúrese de detectar el cambio a través de APISet u otra API expuesta tal como la crea el equipo de características, y no use la versión como proxy para alguna característica o corrección.</span><span class="sxs-lookup"><span data-stu-id="52db0-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="52db0-121">Si hay cambios importantes y no se expone una comprobación adecuada, se trata de un error.</span><span class="sxs-lookup"><span data-stu-id="52db0-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="52db0-122">Asegúrese de que la aplicación no comprueba la versión de maneras impares, como por ejemplo, a través del registro, versiones de archivo, desplazamientos, modo kernel, controladores u otros medios.</span><span class="sxs-lookup"><span data-stu-id="52db0-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="52db0-123">Si la aplicación necesita comprobar la versión, use las API GetVersion, que deben devolver el número principal, secundario y de compilación.</span><span class="sxs-lookup"><span data-stu-id="52db0-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="52db0-124">Si usa la API GetVersion u otras funciones auxiliares de versiones como [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), recuerde que el comportamiento de esta API ha cambiado a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="52db0-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="52db0-125">Consulte [la documentación de la API](../SysInfo/version-helper-apis.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="52db0-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="52db0-126">Si tiene aplicaciones como antimalware o firewall, debe trabajar con sus canales de comentarios habituales y a través del programa Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="52db0-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="52db0-127">Declarar la compatibilidad de Windows 10 con un manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="52db0-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="52db0-128">Si la aplicación es compatible con Windows 10, puede declarar este hecho en el manifiesto de la [aplicación (ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="52db0-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="52db0-129">Esto indica al sistema que la aplicación entiende el número de versión del sistema de Windows 10 de 10,0 (por lo que la API GetVersion no devuelve una versión anterior) y también permite al sistema desactivar otros comportamientos de compatibilidad aplicados a las aplicaciones que no declaran la compatibilidad con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="52db0-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="52db0-130">Para declarar la compatibilidad de Windows 10 en un manifiesto de aplicación, deberá agregar una [sección de **&lt; &gt; compatibilidad**](../SbsCs/application-manifests.md#compatibility) del manifiesto si aún no existe uno **&lt; &gt;** y, después, agregar los elementos admitidos para Windows 10 y todas las demás versiones de Windows que quiera declarar que admita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="52db0-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="52db0-131">En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que admite todas las versiones de Windows de Windows Vista a Windows 10:</span><span class="sxs-lookup"><span data-stu-id="52db0-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
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
</assembly>
```

<span data-ttu-id="52db0-132">La línea anterior marcada `* ADD THIS LINE *` muestra cómo dirigirse con precisión a la aplicación para Windows 10.</span><span class="sxs-lookup"><span data-stu-id="52db0-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="52db0-133">La declaración de compatibilidad con Windows 10 en el manifiesto de la aplicación no tendrá ningún efecto cuando se ejecute la aplicación en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="52db0-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="52db0-134">Recursos</span><span class="sxs-lookup"><span data-stu-id="52db0-134">Resources</span></span>

-   [<span data-ttu-id="52db0-135">Descarga del kit de herramientas de compatibilidad de aplicaciones: Descargar Windows ADK para Windows 10</span><span class="sxs-lookup"><span data-stu-id="52db0-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="52db0-136">[Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="52db0-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="52db0-137">API de aplicaciones auxiliares de versión</span><span class="sxs-lookup"><span data-stu-id="52db0-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)