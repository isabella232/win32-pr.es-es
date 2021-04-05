---
description: En la tabla siguiente se enumeran los
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Herramientas de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001962"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="5232e-103">Herramientas de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="5232e-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="5232e-104">Herramientas de recopilación de datos</span><span class="sxs-lookup"><span data-stu-id="5232e-104">Data collection tools</span></span>

<span data-ttu-id="5232e-105">Las herramientas siguientes son útiles cuando se consumen o manipulan datos del contador de rendimiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="5232e-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="5232e-106">Herramienta</span><span class="sxs-lookup"><span data-stu-id="5232e-106">Tool</span></span>|<span data-ttu-id="5232e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5232e-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="5232e-108">PerfMon</span><span class="sxs-lookup"><span data-stu-id="5232e-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="5232e-109">Herramienta de GUI para recopilar y ver los datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5232e-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="5232e-110">`perfmon.exe` inicia MMC con el complemento monitor de rendimiento, que proporciona acceso al monitor de rendimiento, los conjuntos de recopiladores de datos y las herramientas de informes.</span><span class="sxs-lookup"><span data-stu-id="5232e-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="5232e-111">TypePerf</span><span class="sxs-lookup"><span data-stu-id="5232e-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="5232e-112">Herramienta de línea de comandos para recopilar e imprimir datos de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5232e-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="5232e-113">Se puede usar para enumerar los contraconjuntos disponibles, enumerar los contadores disponibles, imprimir los datos de contador en la consola o recopilar datos de contadores en un archivo de registro (CSV, TDF, BLG).</span><span class="sxs-lookup"><span data-stu-id="5232e-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="5232e-114">Registro</span><span class="sxs-lookup"><span data-stu-id="5232e-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="5232e-115">Herramienta de línea de comandos para transformar y combinar archivos de registro (CSV, TDF, BLG) capturados mediante `typeperf.exe` o a través de las `PDH.dll` API.</span><span class="sxs-lookup"><span data-stu-id="5232e-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="5232e-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="5232e-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="5232e-117">Herramienta de línea de comandos para controlar conjuntos de recopiladores de datos.</span><span class="sxs-lookup"><span data-stu-id="5232e-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="5232e-118">Herramientas del proveedor de datos</span><span class="sxs-lookup"><span data-stu-id="5232e-118">Data provider tools</span></span>

<span data-ttu-id="5232e-119">Las herramientas siguientes son útiles cuando se publican datos del contador de rendimiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="5232e-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="5232e-120">Herramienta</span><span class="sxs-lookup"><span data-stu-id="5232e-120">Tool</span></span>|<span data-ttu-id="5232e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5232e-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="5232e-122">CtrPP</span><span class="sxs-lookup"><span data-stu-id="5232e-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="5232e-123">Herramienta de compilación de línea de comandos de la Windows SDK que valida y compila el manifiesto de proveedor de los contadores de rendimiento V2.</span><span class="sxs-lookup"><span data-stu-id="5232e-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="5232e-124">Esta herramienta genera los `.h` encabezados y los `.rc` scripts de recursos necesarios para compilar un proveedor V2.</span><span class="sxs-lookup"><span data-stu-id="5232e-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="5232e-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="5232e-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="5232e-126">Herramienta de línea de comandos que se usa para instalar el proveedor en un sistema.</span><span class="sxs-lookup"><span data-stu-id="5232e-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="5232e-127">UnlodCtr</span><span class="sxs-lookup"><span data-stu-id="5232e-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="5232e-128">Herramienta de línea de comandos que se usa para desinstalar el proveedor de un sistema.</span><span class="sxs-lookup"><span data-stu-id="5232e-128">Command-line tool used to uninstall your provider from a system.</span></span>
