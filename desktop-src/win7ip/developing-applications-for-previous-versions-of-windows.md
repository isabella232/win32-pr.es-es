---
title: Desarrollo de aplicaciones para versiones anteriores de Windows
description: Explica qué hacer para desarrollar aplicaciones que se ejecutan en versiones anteriores de Windows y aprovechar las ventajas de la API que se admiten con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104424159"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="3dbbf-103">Desarrollo de aplicaciones para versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="3dbbf-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="3dbbf-104">Explica qué hacer para desarrollar aplicaciones que se ejecutan en versiones anteriores de Windows y aprovechar las ventajas de la API que se admiten con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="3dbbf-105">Descargas necesarias</span><span class="sxs-lookup"><span data-stu-id="3dbbf-105">Required Downloads</span></span>

<span data-ttu-id="3dbbf-106">La descarga e instalación de los paquetes que se describen en las siguientes secciones es necesaria si desea desarrollar aplicaciones que usan la API que se introdujeron con el kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="3dbbf-107">Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3dbbf-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="3dbbf-108">La Windows SDK para Windows 7 es necesaria para crear aplicaciones que usan las API compatibles con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="3dbbf-109">Para obtener acceso a recursos e información adicionales, como descargas, publicaciones de foros y el blog del equipo de Windows SDK, consulte el [Centro para desarrolladores de Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3dbbf-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="3dbbf-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="3dbbf-110">.NET Framework</span></span>

<span data-ttu-id="3dbbf-111">Se necesita el Service Pack 1 de .NET Framework 3,5 para crear aplicaciones que usan las API admitidas por la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="3dbbf-112">Para obtener más recursos e información, vea el [Centro para desarrolladores de .NET Framework](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3dbbf-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="3dbbf-113">DirectX SDK necesario al usar Direct3D</span><span class="sxs-lookup"><span data-stu-id="3dbbf-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="3dbbf-114">Si crea aplicaciones que usan Direct3D, el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) es necesario para crear aplicaciones que usan las API admitidas por la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="3dbbf-115">Actualización del equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="3dbbf-115">Update Your Development Computer</span></span>

<span data-ttu-id="3dbbf-116">Asegúrese de que el equipo de desarrollo tenga todas las actualizaciones más recientes de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="3dbbf-117">Si va a desarrollar aplicaciones en una versión anterior de Windows, debe obtener la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 desde Windows Update.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="3dbbf-118">La instalación de cualquiera de estas actualizaciones le permitirá aprovechar la nueva API proporcionada por el Windows SDK para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="3dbbf-119">Para obtener más información acerca de cómo obtener actualizaciones de Windows Update vea el [artículo de Knowledge Base acerca de la actualización de la plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .</span><span class="sxs-lookup"><span data-stu-id="3dbbf-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="3dbbf-120">Entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="3dbbf-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="3dbbf-121">Establecer el destino de compilación en Windows 7</span><span class="sxs-lookup"><span data-stu-id="3dbbf-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="3dbbf-122">Todas las aplicaciones que usan bibliotecas en la actualización de la plataforma para Windows Vista deben compilarse en la plataforma de destino de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="3dbbf-123">Establecer WINVER en el valor de la plataforma de destino de Windows 7 le permite desarrollar aplicaciones que usan las API compatibles con la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 en una máquina de desarrollo que ejecuta Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="3dbbf-124">Puede establecer la plataforma de destino en Windows 7, ya sea en el código fuente o mediante la opción/D con el compilador de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="3dbbf-125">En el ejemplo siguiente se muestra cómo establecer WINVER en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="3dbbf-126">En el ejemplo siguiente se muestra cómo establecer WINVER mediante la opción del compilador/D.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="3dbbf-127">Implementación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="3dbbf-127">Application Deployment</span></span>

<span data-ttu-id="3dbbf-128">Si compila la aplicación mediante los encabezados y las bibliotecas proporcionadas por el Windows SDK para Windows 7, las API admitidas se ejecutarán en cualquier versión de Windows que tenga instalada la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="3dbbf-129">El comportamiento, el rendimiento o los requisitos de algunas API que son compatibles con la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 pueden variar en diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="3dbbf-130">Para obtener más información acerca de una API específica que es compatible con las actualizaciones, vea acerca de la [actualización de la plataforma para Windows Vista](platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3dbbf-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="3dbbf-131">No hay componentes redistribuibles</span><span class="sxs-lookup"><span data-stu-id="3dbbf-131">No Redistributable Components</span></span>

<span data-ttu-id="3dbbf-132">No es necesario que la aplicación Instale componentes redistribuibles, como archivos dll u otros archivos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="3dbbf-133">Requiere End-User equipo actualizado</span><span class="sxs-lookup"><span data-stu-id="3dbbf-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="3dbbf-134">Dado que la actualización de la plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 se hospedan en Windows Update, es muy probable que los usuarios finales con actualizaciones automáticas habilitadas ya tengan estas actualizaciones y los Service Packs necesarios.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="3dbbf-135">Si el equipo del usuario final no tiene instalada la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 y la aplicación requiere API compatibles con estas actualizaciones, es posible que la aplicación no se pueda ejecutar en el equipo del usuario final o que se produzcan errores durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="3dbbf-136">Para evitar los problemas que podrían deberse a que el equipo del usuario no está actualizado, desea comprobar que el equipo del usuario tiene la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 durante la instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="3dbbf-137">Puede usar la [API del agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client) para comprobar si el equipo del usuario final tiene actualizaciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="3dbbf-138">También puede usar la API del agente de Windows Update para descargar e instalar las actualizaciones necesarias durante la instalación de la aplicación si el usuario final no ha instalado ya las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="3dbbf-139">Para obtener un ejemplo de un instalador que muestra cómo usar la [API del agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client), vea [implementación de Direct3D 11 para desarrolladores de juegos](../direct3darticles/direct3d11-deployment.md) en el SDK de [DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3dbbf-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="3dbbf-140">Aunque el ejemplo de instalador de D3D11InstallHelper que se describe en [implementación de Direct3D 11 para desarrolladores de juegos](../direct3darticles/direct3d11-deployment.md)se ha escrito para aplicaciones que usan Direct3D 11, proporciona un buen ejemplo de cómo interactuar con el [Windows Update API del agente](/windows/desktop/Wua_Sdk/portal-client) para iniciar y realizar un seguimiento de la descarga e instalación de actualizaciones que se hospedan en Windows Update.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="3dbbf-141">La compilación de este ejemplo puede requerir el Windows SDK para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="3dbbf-142">Para obtener información adicional sobre el ejemplo D3D11InstallHelper, incluidos los problemas conocidos, consulte el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) notas de la versión de agosto de 2009. actualización de la plataforma para Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="3dbbf-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dbbf-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3dbbf-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dbbf-144">Actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dbbf-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="3dbbf-145">**Temas de introducción**</span><span class="sxs-lookup"><span data-stu-id="3dbbf-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="3dbbf-146">Acerca de la actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dbbf-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="3dbbf-147">Artículo de Knowledge Base acerca de la actualización de la plataforma para Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="3dbbf-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 