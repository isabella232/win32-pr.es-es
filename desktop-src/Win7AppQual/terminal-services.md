---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servicios de Escritorio remoto (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717446"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="c660a-103">Servicios de Escritorio remoto (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="c660a-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c660a-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="c660a-104">Affected Platforms</span></span>

<span data-ttu-id="c660a-105">**Servidores** : windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c660a-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="c660a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c660a-106">Description</span></span>

<span data-ttu-id="c660a-107">Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permite que varios usuarios simultáneos obtengan acceso a Windows Server para proporcionar servicios de hospedaje de aplicaciones y datos mediante la tecnología de "virtualización de presentación" de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c660a-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="c660a-108">Aunque la mayoría de las aplicaciones de 32 y 64 bits se ejecutan tal cual en Windows Servicios de Escritorio remoto, algunas otras no funcionan según lo esperado debido a la diferencia en la plataforma (entorno multiusuario, acceso simultáneo de varios usuarios, etc.).</span><span class="sxs-lookup"><span data-stu-id="c660a-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="c660a-109">Para obtener más información sobre la calidad de la aplicación, consulte las notas del producto sobre la *preparación de la aplicación para Terminal Services* .</span><span class="sxs-lookup"><span data-stu-id="c660a-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="c660a-110">Visite la página del Servicios de Escritorio remoto de productos y los sitios web TechNet de TS más información sobre Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c660a-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="c660a-111">Para obtener más información sobre el desarrollo de aplicaciones para Servicios de Escritorio remoto, revise las *instrucciones de programación de Terminal Services*.</span><span class="sxs-lookup"><span data-stu-id="c660a-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="c660a-112">(Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones).</span><span class="sxs-lookup"><span data-stu-id="c660a-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="c660a-113">Manifiesto de impactos y sus mitigaciones</span><span class="sxs-lookup"><span data-stu-id="c660a-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="c660a-114">Tres cambios en Windows 7 afectan a las aplicaciones en Servicios de Escritorio remoto:</span><span class="sxs-lookup"><span data-stu-id="c660a-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="c660a-115">Windows Server 2008 R2 es solo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c660a-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="c660a-116">Virtualización de IP por sesión</span><span class="sxs-lookup"><span data-stu-id="c660a-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="c660a-117">Implementaciones basadas en MSI: claves específicas del usuario</span><span class="sxs-lookup"><span data-stu-id="c660a-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="c660a-118">**64 solo bits de Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c660a-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="c660a-119">Las aplicaciones escritas para el servidor de 32 bits se ejecutarán en modo WoW y no de forma nativa en Windows Server 2008 R2 o, por lo tanto, en Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c660a-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="c660a-120">Para obtener más información, vea el tema Windows 7 64-bit only.</span><span class="sxs-lookup"><span data-stu-id="c660a-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="c660a-121">*Mitigaciones solo para Windows Server 2008 R2 de 64 bits*</span><span class="sxs-lookup"><span data-stu-id="c660a-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="c660a-122">La mayoría de las aplicaciones escritas para 32 bits seguirán funcionando de la forma habitual en el modo WoW.</span><span class="sxs-lookup"><span data-stu-id="c660a-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="c660a-123">Todas las aplicaciones nuevas escritas para Windows 7 Servicios de Escritorio remoto deben desarrollarse y probarse para su implementación en plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c660a-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="c660a-124">**Virtualización de IP**</span><span class="sxs-lookup"><span data-stu-id="c660a-124">**IP Virtualization**</span></span>

<span data-ttu-id="c660a-125">Virtualización de IP de Escritorio remoto permite al usuario asignar direcciones IP a las conexiones de escritorio remoto por sesión o por programa:</span><span class="sxs-lookup"><span data-stu-id="c660a-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="c660a-126">Si asigna direcciones IP por sesión, todas las aplicaciones usarán la dirección IP de sesión.</span><span class="sxs-lookup"><span data-stu-id="c660a-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="c660a-127">Si asigna direcciones IP por programa, solo las aplicaciones especificadas usarán la dirección IP de sesión y las demás aplicaciones de la sesión no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="c660a-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="c660a-128">Si asigna direcciones IP para varios programas, compartirán una dirección IP de sesión.</span><span class="sxs-lookup"><span data-stu-id="c660a-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="c660a-129">Si tiene más de un adaptador de red en el equipo, también debe elegir uno de ellos para Virtualización de IP de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c660a-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="c660a-130">*Mitigaciones para la virtualización de IP*</span><span class="sxs-lookup"><span data-stu-id="c660a-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="c660a-131">Algunos programas requieren una dirección IP única para cada instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c660a-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="c660a-132">Antes de Windows Server 2008 R2, todas las sesiones de un servidor de escritorio remoto compartían la misma dirección IP, lo que da lugar a problemas de compatibilidad para estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c660a-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="c660a-133">Virtualización de IP de Escritorio remoto permite que estas aplicaciones se ejecuten en un servidor de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c660a-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="c660a-134">**Implementaciones basadas en MSI**</span><span class="sxs-lookup"><span data-stu-id="c660a-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="c660a-135">Compatibilidad de RDS de Microsoft Installer es una característica nueva incluida en Servicios de Escritorio remoto en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c660a-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="c660a-136">Con Servicios de Escritorio remoto en Windows Server 2008 R2, las instalaciones de aplicaciones por usuario las pone en cola el servidor de Escritorio remoto y, a continuación, las controla el instalador de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c660a-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="c660a-137">En Windows Server 2008 R2, puede instalar un programa en el servidor de Escritorio remoto de la misma forma que lo haría en un escritorio local.</span><span class="sxs-lookup"><span data-stu-id="c660a-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="c660a-138">Sin embargo, asegúrese de instalar el programa para todos los usuarios e instalar todos los componentes del programa localmente en el servidor de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c660a-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="c660a-139">*Mitigaciones para implementaciones basadas en MSI*</span><span class="sxs-lookup"><span data-stu-id="c660a-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="c660a-140">Antes de la versión de Windows Server 2008 R2 de Servicios de Escritorio remoto, Windows solo admitía una instalación de Windows Installer a la vez.</span><span class="sxs-lookup"><span data-stu-id="c660a-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="c660a-141">En el caso de las aplicaciones que requieren configuraciones por usuario, como Microsoft Office Word, un administrador necesitaba preinstalar la aplicación y los desarrolladores de aplicaciones necesitaban probar estas aplicaciones en el cliente de escritorio remoto y en el host de sesión de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c660a-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="c660a-142">Windows Installer característica compatibilidad de RDS permite identificar e instalar configuraciones por usuario que faltan para varios usuarios simultáneamente y hace que la experiencia de instalación de la aplicación en Escritorio remoto servidor sea similar a la de un escritorio local.</span><span class="sxs-lookup"><span data-stu-id="c660a-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="c660a-143">**Windows Server 2008 R2 con el rol de [servicios de escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="c660a-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="c660a-144">Se produce un error en una instalación de varios paquetes mediante la [tabla MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) si está habilitado el rol [servicios de escritorio remoto](../termserv/terminal-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c660a-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c660a-145">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="c660a-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="c660a-146">Instrucciones de programación de Terminal Services</span><span class="sxs-lookup"><span data-stu-id="c660a-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="c660a-147">Terminal Services Página principal del producto</span><span class="sxs-lookup"><span data-stu-id="c660a-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="c660a-148">Preparación de la aplicación para Terminal Services notas del producto</span><span class="sxs-lookup"><span data-stu-id="c660a-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="c660a-149">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="c660a-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
