---
description: A partir de Windows 8, la \_ infraestructura de archivos dll de Appinit está deshabilitada cuando el arranque seguro está habilitado.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: Archivos dll de AppInit y arranque seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688481"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="d8448-103">Archivos dll de AppInit y arranque seguro</span><span class="sxs-lookup"><span data-stu-id="d8448-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="d8448-104">A partir de Windows 8, la \_ infraestructura de archivos dll de Appinit está deshabilitada cuando el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d8448-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="d8448-105">Acerca de los \_ archivos dll de Appinit</span><span class="sxs-lookup"><span data-stu-id="d8448-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="d8448-106">La \_ infraestructura de archivos dll de Appinit proporciona una manera sencilla de enlazar las API del sistema al permitir la carga de archivos dll personalizados en el espacio de direcciones de cada aplicación interactiva.</span><span class="sxs-lookup"><span data-stu-id="d8448-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="d8448-107">Las aplicaciones y el software malintencionado usan archivos dll de AppInit para la misma razón básica, que consiste en enlazar las API; una vez cargado el archivo DLL personalizado, puede enlazar una API del sistema conocida e implementar una funcionalidad alternativa.</span><span class="sxs-lookup"><span data-stu-id="d8448-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="d8448-108">Solo un pequeño conjunto de aplicaciones legítimas modernas usa este mecanismo para cargar archivos dll, mientras que un gran conjunto de malware usa este mecanismo para poner en peligro los sistemas.</span><span class="sxs-lookup"><span data-stu-id="d8448-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="d8448-109">Incluso los \_ archivos dll de Appinit legítimos pueden causar involuntariamente interbloqueos del sistema y problemas de rendimiento, por lo que \_ no se recomienda el uso de archivos dll de Appinit.</span><span class="sxs-lookup"><span data-stu-id="d8448-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="d8448-110">\_Archivos dll de Appinit y arranque seguro</span><span class="sxs-lookup"><span data-stu-id="d8448-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="d8448-111">Windows 8 adoptó UEFI y el arranque seguro para mejorar la integridad global del sistema y proporcionar una protección segura contra amenazas sofisticadas.</span><span class="sxs-lookup"><span data-stu-id="d8448-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="d8448-112">Cuando el arranque seguro está habilitado, el \_ mecanismo de archivos dll de Appinit está deshabilitado como parte de un enfoque sin compromiso para proteger a los clientes contra malware y amenazas.</span><span class="sxs-lookup"><span data-stu-id="d8448-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="d8448-113">Tenga en cuenta que el arranque seguro es un protocolo UEFI y no una característica de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8448-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="d8448-114">Puede encontrar más información sobre UEFI y la especificación del Protocolo de arranque seguro en [https://www.uefi.org](https://www.uefi.org/) .</span><span class="sxs-lookup"><span data-stu-id="d8448-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="d8448-115">\_Requisito de certificación de dll de Appinit para aplicaciones de escritorio de Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8448-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="d8448-116">Uno de los requisitos de certificación para aplicaciones de escritorio de Windows 8 es que la aplicación no debe cargar archivos dll arbitrarios para interceptar llamadas a la API de Win32 mediante el \_ mecanismo de archivos dll de Appinit.</span><span class="sxs-lookup"><span data-stu-id="d8448-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="d8448-117">Para obtener información más detallada sobre los requisitos de certificación, consulte la sección 1,1 de [requisitos de certificación para aplicaciones de escritorio de Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="d8448-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="d8448-118">Resumen</span><span class="sxs-lookup"><span data-stu-id="d8448-118">Summary</span></span>

-   <span data-ttu-id="d8448-119">El \_ mecanismo de archivos dll de Appinit no es un enfoque recomendado para aplicaciones legítimas porque puede provocar interbloqueos del sistema y problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d8448-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="d8448-120">El \_ mecanismo de archivos dll de Appinit está deshabilitado de forma predeterminada cuando el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d8448-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="d8448-121">El uso \_ de archivos dll de Appinit en una aplicación de escritorio de Windows 8 es un error de certificación de la aplicación de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="d8448-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="d8448-122">Consulte las siguientes notas del producto para obtener información sobre los \_ archivos dll de Appinit en Windows 7 y Windows server 2008 R2: [AppInit dll en Windows 7 y windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8448-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
