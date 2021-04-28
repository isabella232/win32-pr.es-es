---
description: Servicios de Escritorio remoto (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servicios de Escritorio remoto (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116123"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="08718-103">Servicios de Escritorio remoto (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="08718-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="08718-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="08718-104">Affected Platforms</span></span>

<span data-ttu-id="08718-105">**Servidores:** Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08718-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="08718-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="08718-106">Description</span></span>

<span data-ttu-id="08718-107">Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permite que varios usuarios simultáneos accedan a Windows Server con el fin de proporcionar servicios de hospedaje de datos y aplicaciones mediante la tecnología "Presentation Virtualization" de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="08718-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="08718-108">Aunque la mayoría de las aplicaciones de 32 y 64 bits se ejecutan tal y como están en Windows Servicios de Escritorio remoto, otras no se ejecutan según lo previsto debido a la diferencia en la plataforma (entorno de varios usuarios, acceso simultáneo por varios usuarios, etc.).</span><span class="sxs-lookup"><span data-stu-id="08718-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="08718-109">Para obtener más información sobre la calidad de la aplicación, lea las *white paper de Application Readiness for Terminal Services.*</span><span class="sxs-lookup"><span data-stu-id="08718-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="08718-110">Visite la página Servicios de Escritorio remoto producto y los sitios web de TechNet de TS más información sobre Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="08718-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="08718-111">Para obtener más información sobre el desarrollo de aplicaciones para Servicios de Escritorio remoto, revise las Directrices *de programación de Terminal Services*.</span><span class="sxs-lookup"><span data-stu-id="08718-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="08718-112">(Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones).</span><span class="sxs-lookup"><span data-stu-id="08718-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="08718-113">Demostración de impactos y sus mitigaciones</span><span class="sxs-lookup"><span data-stu-id="08718-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="08718-114">Tres cambios en Windows 7 afectan a las aplicaciones en Servicios de Escritorio remoto:</span><span class="sxs-lookup"><span data-stu-id="08718-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="08718-115">Windows Server 2008 R2 es solo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="08718-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="08718-116">Virtualización de IP por sesión</span><span class="sxs-lookup"><span data-stu-id="08718-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="08718-117">Implementaciones basadas en MSI: claves específicas del usuario</span><span class="sxs-lookup"><span data-stu-id="08718-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="08718-118">**Solo Windows Server 2008 R2 de 64 bits**</span><span class="sxs-lookup"><span data-stu-id="08718-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="08718-119">Las aplicaciones escritas para el servidor de 32 bits se ejecutarán en modo WoW y no de forma nativa en Windows Server 2008 R2 o, por lo tanto, en Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="08718-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="08718-120">Consulte el tema Solo Windows 7 de 64 bits para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="08718-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="08718-121">*Mitigaciones solo para Windows Server 2008 R2 de 64 bits*</span><span class="sxs-lookup"><span data-stu-id="08718-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="08718-122">La mayoría de las aplicaciones escritas para 32 bits seguirán funcionando con normalidad en el modo WoW.</span><span class="sxs-lookup"><span data-stu-id="08718-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="08718-123">Todas las nuevas aplicaciones escritas para Windows 7 Servicios de Escritorio remoto deben desarrollarse y probarse para su implementación en plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="08718-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="08718-124">**Virtualización de IP**</span><span class="sxs-lookup"><span data-stu-id="08718-124">**IP Virtualization**</span></span>

<span data-ttu-id="08718-125">Virtualización de IP de Escritorio remoto permite al usuario asignar direcciones IP a conexiones de Escritorio remoto por sesión o por programa:</span><span class="sxs-lookup"><span data-stu-id="08718-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="08718-126">Si asigna direcciones IP por sesión, todas las aplicaciones usarán la dirección IP de la sesión.</span><span class="sxs-lookup"><span data-stu-id="08718-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="08718-127">Si asigna direcciones IP por programa, solo las aplicaciones especificadas usarán la dirección IP de sesión y las aplicaciones restantes de la sesión no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="08718-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="08718-128">Si asigna direcciones IP para varios programas, compartirán una dirección IP de sesión.</span><span class="sxs-lookup"><span data-stu-id="08718-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="08718-129">Si tiene más de un adaptador de red en el equipo, también debe elegir uno de ellos para Virtualización de IP de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="08718-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="08718-130">*Mitigaciones de virtualización de IP*</span><span class="sxs-lookup"><span data-stu-id="08718-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="08718-131">Algunos programas requieren una dirección IP única para cada instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08718-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="08718-132">Antes de Windows Server 2008 R2, todas las sesiones de un servidor de Escritorio remoto compartían la misma dirección IP, lo que provocaba problemas de compatibilidad para estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="08718-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="08718-133">Virtualización de IP de Escritorio remoto permite que estas aplicaciones se ejecuten en un Escritorio remoto Server.</span><span class="sxs-lookup"><span data-stu-id="08718-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="08718-134">**Implementaciones basadas en MSI**</span><span class="sxs-lookup"><span data-stu-id="08718-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="08718-135">Compatibilidad con RDS de Microsoft Installer es una nueva característica incluida Servicios de Escritorio remoto en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="08718-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="08718-136">Con Servicios de Escritorio remoto en Windows Server 2008 R2, el servidor de Escritorio remoto pone en cola las instalaciones de aplicaciones por usuario y, a continuación, las administra Microsoft Installer.</span><span class="sxs-lookup"><span data-stu-id="08718-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="08718-137">En Windows Server 2008 R2, puede instalar un programa en Escritorio remoto Server igual que instalaría el programa en un escritorio local.</span><span class="sxs-lookup"><span data-stu-id="08718-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="08718-138">Sin embargo, asegúrese de instalar el programa para todos los usuarios e instalar todos los componentes del programa localmente en Escritorio remoto Server.</span><span class="sxs-lookup"><span data-stu-id="08718-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="08718-139">*Mitigaciones para implementaciones basadas en MSI*</span><span class="sxs-lookup"><span data-stu-id="08718-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="08718-140">Antes de la versión de Windows Server 2008 R2 de Servicios de Escritorio remoto, Windows solo Windows Installer instalación a la vez.</span><span class="sxs-lookup"><span data-stu-id="08718-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="08718-141">En el caso de las aplicaciones que requerían configuraciones por usuario, como Microsoft Office Word, un administrador necesitaba instalar previamente la aplicación y los desarrolladores de aplicaciones necesitaban probar estas aplicaciones en el cliente de Escritorio remoto y en el host de sesión de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="08718-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="08718-142">Windows Installer compatibilidad con RDS permite identificar e instalar configuraciones por usuario que faltan para varios usuarios simultáneamente y hace que la experiencia de instalación de la aplicación en Escritorio remoto Server sea similar a la de un escritorio local.</span><span class="sxs-lookup"><span data-stu-id="08718-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="08718-143">**Windows Server 2008 R2 con el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No se admite.</span><span class="sxs-lookup"><span data-stu-id="08718-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="08718-144">Se produce un error en una instalación de varios paquetes mediante la tabla [MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) si el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) está habilitado.</span><span class="sxs-lookup"><span data-stu-id="08718-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="08718-145">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="08718-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="08718-146">Directrices de programación de Terminal Services</span><span class="sxs-lookup"><span data-stu-id="08718-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="08718-147">Página principal del producto terminal Services</span><span class="sxs-lookup"><span data-stu-id="08718-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="08718-148">Documento técnico de Preparación de la aplicación para Terminal Services</span><span class="sxs-lookup"><span data-stu-id="08718-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="08718-149">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="08718-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
