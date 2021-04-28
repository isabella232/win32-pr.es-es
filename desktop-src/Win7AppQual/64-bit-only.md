---
description: Solo 64 bits
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088813"
---
# <a name="64-bit-only"></a><span data-ttu-id="e1263-103">Solo 64 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e1263-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="e1263-104">Affected Platforms</span></span>

<span data-ttu-id="e1263-105">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1263-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="e1263-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="e1263-106">Feature Impact</span></span>

 <span data-ttu-id="e1263-107">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="e1263-107">**Severity** - Low</span></span>  
<span data-ttu-id="e1263-108">**Frecuencia:** alta</span><span class="sxs-lookup"><span data-stu-id="e1263-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="e1263-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1263-109">Description</span></span>

<span data-ttu-id="e1263-110">Windows Server 2008 R2 se distribuye solo con una SKU de 64 bits; no hay ninguna SKU de 32 bits disponible para la versión del servidor del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1263-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="e1263-111">Sin embargo, una SKU de 32 bits sigue estando disponible para el cliente de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1263-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e1263-112">Demostración del impacto</span><span class="sxs-lookup"><span data-stu-id="e1263-112">Manifestation of Impact</span></span>

<span data-ttu-id="e1263-113">Esto afectará a tres áreas:</span><span class="sxs-lookup"><span data-stu-id="e1263-113">This will impact three areas:</span></span>

-   <span data-ttu-id="e1263-114">Controladores de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-114">32-bit drivers</span></span>
-   <span data-ttu-id="e1263-115">Complementos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="e1263-116">Ejecutables de 16 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="e1263-117">Solución para controladores de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="e1263-118">Vuelva a compilar controladores de 32 bits como controladores de 64 bits firmados.</span><span class="sxs-lookup"><span data-stu-id="e1263-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="e1263-119">Solución para complementos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="e1263-120">WoW64, un emulador x86, permite que las aplicaciones basadas en Windows de 32 bits se ejecuten sin problemas en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e1263-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="e1263-121">WoW64 es ahora una característica opcional que debe instalar si es necesario ejecutar código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1263-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="e1263-122">El sistema aísla las aplicaciones de 32 bits de las aplicaciones de 64 bits, lo que incluye la prevención de colisiones entre archivos y registros.</span><span class="sxs-lookup"><span data-stu-id="e1263-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="e1263-123">Se admiten aplicaciones de consola, GUI y servicio.</span><span class="sxs-lookup"><span data-stu-id="e1263-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="e1263-124">El sistema proporciona interoperabilidad a través del límite 32/64 para escenarios como cortar y pegar y COM.</span><span class="sxs-lookup"><span data-stu-id="e1263-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="e1263-125">Sin embargo, los procesos de 32 bits no pueden cargar archivos DLL de 64 bits y los procesos de 64 bits no pueden cargar archivos DLL de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1263-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="e1263-126">Normalmente, esto se ve en los complementos de shell escritos para Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1263-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="e1263-127">Una aplicación de 32 bits puede detectar si se ejecuta en WOW64 llamando a la función IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="e1263-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="e1263-128">La aplicación puede obtener información adicional sobre el procesador mediante la función GetNativeSystemInfo</span><span class="sxs-lookup"><span data-stu-id="e1263-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="e1263-129">Tenga en cuenta que Windows de 64 bits no admite la ejecución de aplicaciones basadas en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e1263-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="e1263-130">La razón principal es que los identificadores tienen 32 bits significativos en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e1263-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="e1263-131">Por lo tanto, los identificadores no se pueden truncar y pasar a aplicaciones de 16 bits sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="e1263-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="e1263-132">Los intentos de iniciar aplicaciones de 16 bits producirán el siguiente error: ERROR \_ BAD \_ EXE \_ FORMAT.</span><span class="sxs-lookup"><span data-stu-id="e1263-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="e1263-133">Solución para ejecutables de 16 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="e1263-134">Windows de 64 bits reconoce un número limitado de programas específicos del instalador de 16 bits y sustituye una versión de 32 bits porteada.</span><span class="sxs-lookup"><span data-stu-id="e1263-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="e1263-135">La lista de sustituciones se almacena en el Registro con la siguiente clave: HKEY LOCAL MACHINE Software Microsoft Windows NT CurrentVersion NtVdm64 Hay compatibilidad integrada con varios motores de instalador, incluidos los instaladores de \_ \_ \\ \\ \\ \\ \\ InstallShield 5.x.</span><span class="sxs-lookup"><span data-stu-id="e1263-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="e1263-136">Tenga en cuenta que el Windows Installer de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e1263-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e1263-137">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="e1263-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="e1263-138">Ejecución de aplicaciones de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="e1263-139">Rendimiento y consumo de memoria</span><span class="sxs-lookup"><span data-stu-id="e1263-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="e1263-140">Detalles de implementación de WOW64</span><span class="sxs-lookup"><span data-stu-id="e1263-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="e1263-141">Redirector del Registro</span><span class="sxs-lookup"><span data-stu-id="e1263-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="e1263-142">Redirector del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="e1263-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="e1263-143">Administración de memoria</span><span class="sxs-lookup"><span data-stu-id="e1263-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="e1263-144">Afinidad del procesador</span><span class="sxs-lookup"><span data-stu-id="e1263-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="e1263-145">Comunicación entre procesos</span><span class="sxs-lookup"><span data-stu-id="e1263-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="e1263-146">Instalación de aplicaciones en sistemas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="e1263-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="e1263-147">Depuración wow64</span><span class="sxs-lookup"><span data-stu-id="e1263-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="e1263-148">**Función IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="e1263-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="e1263-149">**GetNativeSystemInfo (Función)**</span><span class="sxs-lookup"><span data-stu-id="e1263-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
