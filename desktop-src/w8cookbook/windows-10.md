---
title: Windows 10
description: En este manual se proporciona información a los desarrolladores sobre los cambios de plataforma en los sistemas operativos Windows 10 (SO).
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421255"
---
# <a name="windows-10"></a><span data-ttu-id="5849e-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5849e-103">Windows 10</span></span>

<span data-ttu-id="5849e-104">En este manual se proporciona información a los desarrolladores sobre los cambios de plataforma en los sistemas operativos Windows 10 (SO).</span><span class="sxs-lookup"><span data-stu-id="5849e-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="5849e-105">También se proporcionan instrucciones para comprobar la compatibilidad de las aplicaciones existentes y planeadas con la versión más reciente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5849e-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="5849e-106">Damos por hecho que está familiarizado con las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="5849e-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="5849e-107">El contenido se aplica a: Windows 10</span><span class="sxs-lookup"><span data-stu-id="5849e-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="5849e-108">La cocina es para desarrolladores de terceros de aplicaciones y dispositivos que están diseñados para usarse en el entorno de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5849e-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="5849e-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="5849e-109">Introduction</span></span>

<span data-ttu-id="5849e-110">Windows 10 presenta la tecnología de sistema operativo y las plataformas de desarrollo de software más recientes para su uso por parte de desarrolladores de aplicaciones y controladores y empresas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="5849e-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="5849e-111">Para mejorar aún más la seguridad, la confiabilidad, el rendimiento y la experiencia del usuario de Windows, Microsoft ha incorporado muchas características nuevas, ha mejorado las características existentes y ha eliminado otras.</span><span class="sxs-lookup"><span data-stu-id="5849e-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="5849e-112">Aunque el objetivo de Windows 10 es mantener la compatibilidad con las aplicaciones escritas para las versiones publicadas anteriormente del sistema operativo Windows, algunas interrupciones de compatibilidad son inevitables debido a innovaciones, seguridad apretada y mayor confiabilidad.</span><span class="sxs-lookup"><span data-stu-id="5849e-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="5849e-113">En general, la compatibilidad de la versión más reciente del sistema operativo Windows con aplicaciones y dispositivos existentes es alta.</span><span class="sxs-lookup"><span data-stu-id="5849e-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="5849e-114">En este documento se muestra cómo comprobar que las aplicaciones y los dispositivos son compatibles con la versión más reciente del sistema operativo y proporciona información general sobre problemas conocidos de incompatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5849e-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="5849e-115">Le invitamos a consultar estos temas para aprender a optimizar sus aplicaciones y aprovechar las ventajas de lo que ofrece esta versión más reciente de Windows.</span><span class="sxs-lookup"><span data-stu-id="5849e-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="5849e-116">Contenido</span><span class="sxs-lookup"><span data-stu-id="5849e-116">Contents</span></span>

-   [<span data-ttu-id="5849e-117">Cambios clave desde Windows 7 para garantizar la compatibilidad</span><span class="sxs-lookup"><span data-stu-id="5849e-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="5849e-118">Cómo podemos asegurar la compatibilidad del ecosistema combinado</span><span class="sxs-lookup"><span data-stu-id="5849e-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="5849e-119">Comprobación de la versión de Windows</span><span class="sxs-lookup"><span data-stu-id="5849e-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="5849e-120">API sin documentar</span><span class="sxs-lookup"><span data-stu-id="5849e-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="5849e-121">Desarrollo de aplicaciones de puente de escritorio y UWP</span><span class="sxs-lookup"><span data-stu-id="5849e-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="5849e-122">La funcionalidad de la aplicación de escritorio moderna se ve afectada si no se ejecuta en modo de ventana</span><span class="sxs-lookup"><span data-stu-id="5849e-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="5849e-123">Disponibilidad de los controladores de gráficos aplicables en Windows Update</span><span class="sxs-lookup"><span data-stu-id="5849e-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="5849e-124">Migración del controlador de gráficos a Windows 10</span><span class="sxs-lookup"><span data-stu-id="5849e-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="5849e-125">Controladores Bluetooth</span><span class="sxs-lookup"><span data-stu-id="5849e-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="5849e-126">Descargar la guía de cocina</span><span class="sxs-lookup"><span data-stu-id="5849e-126">Download the cookbook</span></span>

<span data-ttu-id="5849e-127">Para obtener una referencia rápida a toda esta información, así como información sobre Windows como servicio, compatibilidad con aplicaciones en Windows y estrategias optimizadas para probar la aplicación, [Descargue la guía de compatibilidad de Windows 10](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span><span class="sxs-lookup"><span data-stu-id="5849e-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="5849e-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5849e-128">See Also</span></span>

-   <span data-ttu-id="5849e-129">[Windows como servicio](/windows/deployment/update/), para obtener información sobre los tipos de versión y la compatibilidad con aplicaciones de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5849e-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="5849e-130">[Windows Insider](https://insider.windows.com/), para obtener acceso a las compilaciones de vista previa, probar y proporcionar comentarios.</span><span class="sxs-lookup"><span data-stu-id="5849e-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="5849e-131">[Listo para Windows 10](https://www.readyfor10.com/), para enviar la información de su empresa a un recurso para los administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="5849e-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 