---
title: Servicio de transferencia inteligente en segundo plano
description: El Servicio de transferencia inteligente en segundo plano (BITS) transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información sobre el progreso de las transferencias.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano, página de inicio
- BITS (consulte Servicio de transferencia inteligente en segundo plano)
- descargar archivos BITS
- BITS de transferencia de archivos en segundo plano
- carga de archivos BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 9483e297e8b48ad6466846c7eceb8d53b57d3278
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424215"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="ac4f1-109">Servicio de transferencia inteligente en segundo plano</span><span class="sxs-lookup"><span data-stu-id="ac4f1-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="ac4f1-110">Propósito</span><span class="sxs-lookup"><span data-stu-id="ac4f1-110">Purpose</span></span>

<span data-ttu-id="ac4f1-111">Servicio de transferencia inteligente en segundo plano (BITS) los programadores y administradores del sistema usan para descargar o cargar archivos en servidores web HTTP y recursos compartidos de archivos SMB.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="ac4f1-112">BITS tendrá en cuenta el costo de la transferencia, así como el uso de la red para que el trabajo en primer plano del usuario tenga el menor impacto posible.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="ac4f1-113">BITS también controla las interupciones de red, pausando y reanudando automáticamente las transferencias, incluso después de un reinicio.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="ac4f1-114">BITS incluye cmdlets de PowerShell para crear y administrar transferencias, así como la utilidad de línea de comandos BitsAdmin.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="ac4f1-115">Windows puede usar BITS para descargar actualizaciones en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="ac4f1-116">Si es un usuario final que busca maneras de solucionar problemas de la instalación de BITS, consulte [Corrección de Windows Update problemas.](https://support.microsoft.com/help/10164/fix-windows-update-errors)</span><span class="sxs-lookup"><span data-stu-id="ac4f1-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="ac4f1-117">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="ac4f1-117">Where applicable</span></span>

<span data-ttu-id="ac4f1-118">Use BITS para las aplicaciones que necesitan:</span><span class="sxs-lookup"><span data-stu-id="ac4f1-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="ac4f1-119">Descargue o cargue archivos en un servidor web HTTP o REST o un servidor de archivos SMB.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="ac4f1-120">Reanude automáticamente las transferencias de archivos después de que se desconecte la red y se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="ac4f1-121">Conserve la capacidad de respuesta de otras aplicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="ac4f1-122">Tenga en cuenta el costo de red en, por ejemplo, las redes móviles.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="ac4f1-123">Opcionalmente, trabaje con [BranchCache para](/windows-server/networking/branchcache/branchcache) optimizar el tráfico de red de área extensa (WAN).</span><span class="sxs-lookup"><span data-stu-id="ac4f1-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ac4f1-124">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="ac4f1-124">Developer audience</span></span>

<span data-ttu-id="ac4f1-125">BITS es una interfaz COM diseñada para desarrolladores de C y C++ que también pueden usar los desarrolladores de .NET.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="ac4f1-126">Los desarrolladores de UWP deben usar la API [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) y no la API de BITS.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="ac4f1-127">Versiones de BITS</span><span class="sxs-lookup"><span data-stu-id="ac4f1-127">BITS versions</span></span>

<span data-ttu-id="ac4f1-128">Para obtener un historial completo de versiones e información sobre el sistema operativo anterior, vea [Novedades.](what-s-new.md)</span><span class="sxs-lookup"><span data-stu-id="ac4f1-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="ac4f1-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ac4f1-129">In this section</span></span>



| <span data-ttu-id="ac4f1-130">Tema</span><span class="sxs-lookup"><span data-stu-id="ac4f1-130">Topic</span></span>                                                           | <span data-ttu-id="ac4f1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac4f1-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac4f1-132">Acerca de BITS</span><span class="sxs-lookup"><span data-stu-id="ac4f1-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="ac4f1-133">Información general sobre BITS.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="ac4f1-134">Uso de BITS</span><span class="sxs-lookup"><span data-stu-id="ac4f1-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="ac4f1-135">Guía de procedimientos para desarrollar clientes BITS que transfieren archivos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="ac4f1-136">Referencia de BITS</span><span class="sxs-lookup"><span data-stu-id="ac4f1-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="ac4f1-137">Información de referencia para las interfaces de programación de BITS.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="ac4f1-138">También contiene información sobre ejemplos, herramientas, configuración del servidor para trabajos de carga y el protocolo de carga.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="ac4f1-139">Procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="ac4f1-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="ac4f1-140">Información que se debe tener en cuenta al diseñar una aplicación que usa BITS.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="ac4f1-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ac4f1-141">Additional resources</span></span>

<span data-ttu-id="ac4f1-142">Los siguientes son recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-142">The following are additional resources.</span></span>


|    <span data-ttu-id="ac4f1-143">Recurso</span><span class="sxs-lookup"><span data-stu-id="ac4f1-143">Resource</span></span>         |    <span data-ttu-id="ac4f1-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac4f1-144">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4f1-145">DLL de referencia de .NET</span><span class="sxs-lookup"><span data-stu-id="ac4f1-145">.NET Reference DLL</span></span>   | <span data-ttu-id="ac4f1-146">Para obtener información sobre el uso de BITS desde .NET mediante archivos DLL de referencia, vea Llamar a [BITS desde .NET mediante archivos DLL de referencia.](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="ac4f1-146">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="ac4f1-147">Contenedor de .NET</span><span class="sxs-lookup"><span data-stu-id="ac4f1-147">.NET Wrapper</span></span>   | <span data-ttu-id="ac4f1-148">Para otros contenedores de .NET para BITS, puede buscar [en nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) proyectos etiquetados con la etiqueta BITS.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-148">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

