---
title: Servicio de transferencia inteligente en segundo plano
description: El Servicio de transferencia inteligente en segundo plano (BITS) transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información sobre el progreso de las transferencias.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano, página de inicio
- BITS (vea Servicio de transferencia inteligente en segundo plano)
- descargar BITS de archivos
- BITS de transferencia de archivo en segundo plano
- cargar BITS de archivos
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995502"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="5fba2-109">Servicio de transferencia inteligente en segundo plano</span><span class="sxs-lookup"><span data-stu-id="5fba2-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="5fba2-110">Propósito</span><span class="sxs-lookup"><span data-stu-id="5fba2-110">Purpose</span></span>

<span data-ttu-id="5fba2-111">Los programadores y los administradores del sistema usan Servicio de transferencia inteligente en segundo plano (BITS) para descargar archivos o cargar archivos en los servidores Web HTTP y los recursos compartidos de archivos SMB.</span><span class="sxs-lookup"><span data-stu-id="5fba2-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="5fba2-112">BITS tendrá en cuenta el costo de la transferencia, así como el uso de la red para que el trabajo en primer plano del usuario tenga el menor impacto posible.</span><span class="sxs-lookup"><span data-stu-id="5fba2-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="5fba2-113">BITS también controla la interuptions de red, la pausa y la reanudación automática de las transferencias, incluso después de un reinicio.</span><span class="sxs-lookup"><span data-stu-id="5fba2-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="5fba2-114">BITS incluye cmdlets de PowerShell para crear y administrar transferencias, así como la utilidad de línea de comandos BitsAdmin.</span><span class="sxs-lookup"><span data-stu-id="5fba2-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="5fba2-115">Windows puede usar BITS para descargar actualizaciones en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="5fba2-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="5fba2-116">Si es un usuario final que busca maneras de solucionar problemas de la instalación de BITS, consulte [solución de problemas de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span><span class="sxs-lookup"><span data-stu-id="5fba2-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="5fba2-117">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="5fba2-117">Where applicable</span></span>

<span data-ttu-id="5fba2-118">Use BITS para las aplicaciones que necesitan:</span><span class="sxs-lookup"><span data-stu-id="5fba2-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="5fba2-119">Descargue o cargue archivos en un servidor Web HTTP o REST o en un servidor de archivos SMB.</span><span class="sxs-lookup"><span data-stu-id="5fba2-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="5fba2-120">Reanudar automáticamente las transferencias de archivos después de desconectarse de la red y reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="5fba2-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="5fba2-121">Conservar la capacidad de respuesta de otras aplicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="5fba2-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="5fba2-122">Tenga en cuentan el costo de red en, por ejemplo, las redes móviles</span><span class="sxs-lookup"><span data-stu-id="5fba2-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="5fba2-123">Opcionalmente, puede trabajar con [BranchCache](/windows-server/networking/branchcache/branchcache) para optimizar el tráfico de la red de área extensa (WAN).</span><span class="sxs-lookup"><span data-stu-id="5fba2-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5fba2-124">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="5fba2-124">Developer audience</span></span>

<span data-ttu-id="5fba2-125">BITS es una interfaz COM diseñada para desarrolladores de C y C++ que los desarrolladores de .NET también pueden usar.</span><span class="sxs-lookup"><span data-stu-id="5fba2-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="5fba2-126">Los desarrolladores de UWP deben usar la API [Windows. networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) y no la API de bits.</span><span class="sxs-lookup"><span data-stu-id="5fba2-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="5fba2-127">Versiones de BITS</span><span class="sxs-lookup"><span data-stu-id="5fba2-127">BITS versions</span></span>

<span data-ttu-id="5fba2-128">Para obtener el historial de versiones completo e información sobre el sistema operativo anterior, vea [novedades](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="5fba2-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="5fba2-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5fba2-129">In this section</span></span>



| <span data-ttu-id="5fba2-130">Tema</span><span class="sxs-lookup"><span data-stu-id="5fba2-130">Topic</span></span>                                                           | <span data-ttu-id="5fba2-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fba2-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fba2-132">Acerca de BITS</span><span class="sxs-lookup"><span data-stu-id="5fba2-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="5fba2-133">Información general sobre BITS.</span><span class="sxs-lookup"><span data-stu-id="5fba2-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="5fba2-134">Usar BITS</span><span class="sxs-lookup"><span data-stu-id="5fba2-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="5fba2-135">Guía de procedimientos para desarrollar clientes de BITS que transfieren archivos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="5fba2-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="5fba2-136">Referencia de BITS</span><span class="sxs-lookup"><span data-stu-id="5fba2-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="5fba2-137">Información de referencia de las interfaces de programación de BITS.</span><span class="sxs-lookup"><span data-stu-id="5fba2-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="5fba2-138">También contiene información sobre ejemplos, herramientas, configuración del servidor para trabajos de carga y el protocolo de carga.</span><span class="sxs-lookup"><span data-stu-id="5fba2-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="5fba2-139">Procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="5fba2-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="5fba2-140">Información que se debe tener en cuenta al diseñar una aplicación que usa BITS.</span><span class="sxs-lookup"><span data-stu-id="5fba2-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="5fba2-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5fba2-141">Additional resources</span></span>

<span data-ttu-id="5fba2-142">Los siguientes son recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="5fba2-142">The following are additional resources.</span></span>


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fba2-143">DLL de referencia de .NET</span><span class="sxs-lookup"><span data-stu-id="5fba2-143">.NET Reference DLL</span></span>   | <span data-ttu-id="5fba2-144">Para obtener información sobre el uso de BITS desde .NET mediante el uso de archivos dll de referencia, consulte [llamar a bits desde .net mediante archivos dll de referencia](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="5fba2-144">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="5fba2-145">Contenedor .NET</span><span class="sxs-lookup"><span data-stu-id="5fba2-145">.NET Wrapper</span></span>   | <span data-ttu-id="5fba2-146">En el caso de otros contenedores de .NET para BITS, puede buscar en [Nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) los proyectos etiquetados con la etiqueta bits.</span><span class="sxs-lookup"><span data-stu-id="5fba2-146">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

