---
description: La tecnología de memoria persistente (PM) proporciona acceso de nivel de bytes a medios no volátiles, a la vez que reduce la latencia del almacenamiento o la recuperación de datos de forma significativa.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: 'Programación de memoria persistente en Windows: integración de NVML'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278917"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="f504d-103">Programación de memoria persistente en Windows: integración de NVML</span><span class="sxs-lookup"><span data-stu-id="f504d-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="f504d-104">La tecnología de memoria persistente (PM) proporciona acceso de nivel de bytes a medios no volátiles, a la vez que reduce la latencia del almacenamiento o la recuperación de datos de forma significativa.</span><span class="sxs-lookup"><span data-stu-id="f504d-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="f504d-105">Crea un nuevo nivel entre la memoria del sistema y el almacenamiento tradicional.</span><span class="sxs-lookup"><span data-stu-id="f504d-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="f504d-106">Cualquier programa que dependa o escale con escrituras rápidas en un medio persistente puede beneficiarse de PM.</span><span class="sxs-lookup"><span data-stu-id="f504d-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="f504d-107">El propósito de este artículo es describir cómo se puede integrar la biblioteca de memoria no volátil (NVML) en un proyecto de Visual Studio para facilitar su uso.</span><span class="sxs-lookup"><span data-stu-id="f504d-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="f504d-108">La memoria persistente a veces se conoce también como memoria de clase de almacenamiento (SCM).</span><span class="sxs-lookup"><span data-stu-id="f504d-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="f504d-109">PM y NVML</span><span class="sxs-lookup"><span data-stu-id="f504d-109">PM and NVML</span></span>

<span data-ttu-id="f504d-110">La primera compatibilidad con la memoria persistente se incorporó en Windows Server 2016 y la actualización de aniversario de Windows 10 (1607).</span><span class="sxs-lookup"><span data-stu-id="f504d-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="f504d-111">Para obtener una introducción rápida, eche un vistazo a estos dos vídeos de Channel9:</span><span class="sxs-lookup"><span data-stu-id="f504d-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   [<span data-ttu-id="f504d-112">Uso de memoria no volátil (NVDIMM-N) como almacenamiento en bloque en Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f504d-112">Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P466)
-   [<span data-ttu-id="f504d-113">Uso de memoria no volátil (NVDIMM-N) como almacenamiento Byte-Addressable en Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f504d-113">Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P470)

<span data-ttu-id="f504d-114">Para ayudar a los desarrolladores a aprovechar las ventajas de las ofertas de memoria persistentes, Microsoft también ha contribuido a la realización de la biblioteca de memoria no volátil (NVML) en Windows.</span><span class="sxs-lookup"><span data-stu-id="f504d-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="f504d-115">Esta biblioteca proporciona varias herramientas para hacer que las aplicaciones reconozcan la memoria de forma persistente.</span><span class="sxs-lookup"><span data-stu-id="f504d-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="f504d-116">Por ejemplo, contiene código que le permite crear fácilmente un almacén de clave-valor para PM para búsquedas y almacenes extremadamente rápidos.</span><span class="sxs-lookup"><span data-stu-id="f504d-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="f504d-117">Puede encontrar más información sobre NVML, incluidos ejemplos, en la [biblioteca NVM](https://pmem.io/nvml/).</span><span class="sxs-lookup"><span data-stu-id="f504d-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="f504d-118">Integración de NVML en un proyecto de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f504d-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="f504d-119">Descargar archivos y encabezados de la biblioteca NVML</span><span class="sxs-lookup"><span data-stu-id="f504d-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="f504d-120">NVML se mantiene en GitHub.</span><span class="sxs-lookup"><span data-stu-id="f504d-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="f504d-121">Puede compilar el origen usted mismo o simplemente descargar los archivos binarios compilados directamente desde aquí: [NVML versión 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span><span class="sxs-lookup"><span data-stu-id="f504d-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="f504d-122">Coloque los archivos de biblioteca y los encabezados en un directorio de su elección, por ejemplo: "C: \\ NVML \\ lib" y "c: \\ NVML \\ Inc", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f504d-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="f504d-123">Configure el proyecto de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f504d-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="f504d-124">Abra el proyecto de Visual Studio y, en el "Explorador de soluciones", haga clic con el botón derecho en el nombre del proyecto.</span><span class="sxs-lookup"><span data-stu-id="f504d-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="f504d-125">Abra el panel de configuración del proyecto en la parte inferior del elemento emergente resultante.</span><span class="sxs-lookup"><span data-stu-id="f504d-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="f504d-126">Vaya a "propiedades de configuración-> C/C++" y agregue la carpeta en la que ha almacenado el encabezado (C: \\ NVML \\ Inc) al campo "directorios de inclusión adicionales".</span><span class="sxs-lookup"><span data-stu-id="f504d-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="f504d-127">A continuación, vaya a "propiedades de configuración-> vinculador" y agregue la carpeta en la que ha almacenado la biblioteca (C: \\ NVML \\ lib) al campo "directorios de biblioteca adicionales".</span><span class="sxs-lookup"><span data-stu-id="f504d-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="f504d-128">Después, asegúrese de que tiene como destino el proyecto para Windows Server 2016 o la actualización de aniversario de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="f504d-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="f504d-129">Vaya a "propiedades de configuración-> general" y establezca el campo "versión de la plataforma de destino" en "10.0.14393.0" y</span><span class="sxs-lookup"><span data-stu-id="f504d-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="f504d-130">Vaya a "propiedades de configuración-> C/C++" y agregue "NTDDI \_ version = NTDDI \_ WIN10 \_ RS1;" al campo "preprocesador".</span><span class="sxs-lookup"><span data-stu-id="f504d-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="f504d-131">Incluya los encabezados en el código y vincúlelo a las bibliotecas necesarias.</span><span class="sxs-lookup"><span data-stu-id="f504d-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="f504d-132">En este momento, puede incluir simplemente los archivos de encabezado que desea usar en el código como cualquier otro archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="f504d-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="f504d-133">Por ejemplo, para usar libpmem:</span><span class="sxs-lookup"><span data-stu-id="f504d-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="f504d-134">Agregue " \# include <libpmem. h>" y</span><span class="sxs-lookup"><span data-stu-id="f504d-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="f504d-135">Agregue "libpmem. lib" a "propiedades de configuración-> enlazador-> INPUT-> dependencias adicionales"</span><span class="sxs-lookup"><span data-stu-id="f504d-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="f504d-136">En este momento, está listo para llamar directamente a las funciones de la biblioteca en el código y aprovecharlas.</span><span class="sxs-lookup"><span data-stu-id="f504d-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



