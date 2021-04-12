---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279302"
---
# <a name="64-bit-only"></a><span data-ttu-id="59e39-103">Solo 64 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="59e39-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="59e39-104">Affected Platforms</span></span>

<span data-ttu-id="59e39-105">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59e39-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="59e39-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="59e39-106">Feature Impact</span></span>

 <span data-ttu-id="59e39-107">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="59e39-107">**Severity** - Low</span></span>  
<span data-ttu-id="59e39-108">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="59e39-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="59e39-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="59e39-109">Description</span></span>

<span data-ttu-id="59e39-110">Windows Server 2008 R2 se incluye solo con una SKU de 64 bits; no hay disponible ninguna SKU de 32 bits para la versión de servidor del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="59e39-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="59e39-111">Sin embargo, una SKU de 32 bits sigue estando disponible para el cliente de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59e39-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="59e39-112">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="59e39-112">Manifestation of Impact</span></span>

<span data-ttu-id="59e39-113">Esto afectará a tres áreas:</span><span class="sxs-lookup"><span data-stu-id="59e39-113">This will impact three areas:</span></span>

-   <span data-ttu-id="59e39-114">Controladores de 32 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-114">32-bit drivers</span></span>
-   <span data-ttu-id="59e39-115">Complementos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="59e39-116">ejecutables de 16 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="59e39-117">Solución para los controladores de 32 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="59e39-118">Vuelva a compilar los controladores de 32 bits como controladores de 64 bits firmados.</span><span class="sxs-lookup"><span data-stu-id="59e39-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="59e39-119">Solución para complementos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="59e39-120">WoW64, un emulador de x86, permite que las aplicaciones basadas en Windows de 32 bits se ejecuten sin problemas en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="59e39-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="59e39-121">WoW64 es ahora una característica opcional que se debe instalar si es necesario ejecutar código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="59e39-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="59e39-122">El sistema aísla las aplicaciones de 32 bits de las aplicaciones de 64 bits, lo que incluye evitar colisiones de archivos y del registro.</span><span class="sxs-lookup"><span data-stu-id="59e39-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="59e39-123">Se admiten las aplicaciones de consola, GUI y servicio.</span><span class="sxs-lookup"><span data-stu-id="59e39-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="59e39-124">El sistema proporciona interoperabilidad en el límite de 32/64 para escenarios como cortar y pegar y COM.</span><span class="sxs-lookup"><span data-stu-id="59e39-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="59e39-125">Sin embargo, los procesos de 32 bits no pueden cargar archivos dll de 64 bits y los procesos de 64 bits no pueden cargar archivos dll de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="59e39-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="59e39-126">Normalmente vemos esto en los complementos de Shell escritos para el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="59e39-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="59e39-127">Una aplicación de 32 bits puede detectar si se ejecuta bajo WOW64 mediante una llamada a la función IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="59e39-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="59e39-128">La aplicación puede obtener información adicional sobre el procesador mediante la función GetNativeSystemInfo</span><span class="sxs-lookup"><span data-stu-id="59e39-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="59e39-129">Tenga en cuenta que Windows de 64 bits no admite la ejecución de aplicaciones basadas en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="59e39-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="59e39-130">La razón principal es que los identificadores tienen 32 bits significativos en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="59e39-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="59e39-131">Por lo tanto, los identificadores no se pueden truncar y pasar a las aplicaciones de 16 bits sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="59e39-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="59e39-132">Los intentos de iniciar las aplicaciones de 16 bits producen el siguiente error: ERROR de \_ \_ formato exe incorrecto \_ .</span><span class="sxs-lookup"><span data-stu-id="59e39-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="59e39-133">Solución para archivos ejecutables de 16 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="59e39-134">Windows de 64 bits reconoce un número limitado de programas de instalador de 16 bits específicos y sustituye una versión de 32 bits por puerto.</span><span class="sxs-lookup"><span data-stu-id="59e39-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="59e39-135">La lista de sustituciones se almacena en el registro en la siguiente clave: HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 hay compatibilidad integrada para varios motores de instalación, incluidos los instaladores de InstallShield 5. x.</span><span class="sxs-lookup"><span data-stu-id="59e39-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="59e39-136">Tenga en cuenta que la Windows Installer de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="59e39-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="59e39-137">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="59e39-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="59e39-138">Ejecutar aplicaciones de 32 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="59e39-139">Rendimiento y consumo de memoria</span><span class="sxs-lookup"><span data-stu-id="59e39-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="59e39-140">Detalles de la implementación de WOW64</span><span class="sxs-lookup"><span data-stu-id="59e39-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="59e39-141">Redirector del registro</span><span class="sxs-lookup"><span data-stu-id="59e39-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="59e39-142">Redirector del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="59e39-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="59e39-143">Administración de memoria</span><span class="sxs-lookup"><span data-stu-id="59e39-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="59e39-144">Afinidad del procesador</span><span class="sxs-lookup"><span data-stu-id="59e39-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="59e39-145">Comunicación entre procesos</span><span class="sxs-lookup"><span data-stu-id="59e39-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="59e39-146">Instalación de aplicaciones en sistemas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="59e39-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="59e39-147">Depurar WOW64</span><span class="sxs-lookup"><span data-stu-id="59e39-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="59e39-148">**IsWow64Process función)**</span><span class="sxs-lookup"><span data-stu-id="59e39-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="59e39-149">**GetNativeSystemInfo función)**</span><span class="sxs-lookup"><span data-stu-id="59e39-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
