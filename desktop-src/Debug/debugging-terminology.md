---
description: Los siguientes términos se usan al describir la depuración.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminología de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998061"
---
# <a name="debugging-terminology"></a><span data-ttu-id="022a2-103">Terminología de depuración</span><span class="sxs-lookup"><span data-stu-id="022a2-103">Debugging Terminology</span></span>

<span data-ttu-id="022a2-104">Los siguientes términos se usan al describir la depuración.</span><span class="sxs-lookup"><span data-stu-id="022a2-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="022a2-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Pantalla azul</span><span class="sxs-lookup"><span data-stu-id="022a2-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="022a2-106">Cuando el sistema detecta un problema de hardware, una incoherencia en los datos o un error similar, puede mostrar una pantalla azul que contenga información que se pueda utilizar para determinar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="022a2-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="022a2-107">Esta información incluye el código de detención y si se ha creado un archivo de volcado.</span><span class="sxs-lookup"><span data-stu-id="022a2-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="022a2-108">También puede incluir una lista de los controladores cargados y un seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="022a2-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="022a2-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Archivo de volcado de memoria</span><span class="sxs-lookup"><span data-stu-id="022a2-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="022a2-110">Puede configurar el sistema para escribir información en un archivo de volcado de memoria en el disco duro siempre que se genere un código de detención.</span><span class="sxs-lookup"><span data-stu-id="022a2-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="022a2-111">El archivo contiene información que el depurador puede utilizar para analizar el error.</span><span class="sxs-lookup"><span data-stu-id="022a2-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="022a2-112">Este archivo puede ser tan grande como la memoria física incluida en el equipo.</span><span class="sxs-lookup"><span data-stu-id="022a2-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="022a2-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Depurador</span><span class="sxs-lookup"><span data-stu-id="022a2-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="022a2-114">Programa diseñado para ayudar a detectar, localizar y corregir errores en otro programa.</span><span class="sxs-lookup"><span data-stu-id="022a2-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="022a2-115">Permite al desarrollador recorrer paso a paso la ejecución del proceso y sus subprocesos, la supervisión de la memoria, las variables y otros elementos del contexto del proceso y del subproceso.</span><span class="sxs-lookup"><span data-stu-id="022a2-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="022a2-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modo kernel</span><span class="sxs-lookup"><span data-stu-id="022a2-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="022a2-117">El modo de procesador en el que se ejecutan los servicios del sistema y los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="022a2-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="022a2-118">Todas las interfaces y las instrucciones de CPU están disponibles y se puede tener acceso a toda la memoria.</span><span class="sxs-lookup"><span data-stu-id="022a2-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="022a2-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Archivo de minivolcado</span><span class="sxs-lookup"><span data-stu-id="022a2-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="022a2-120">Las aplicaciones pueden generar archivos de minivolcado en modo usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado.</span><span class="sxs-lookup"><span data-stu-id="022a2-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="022a2-121">Para obtener más información, consulte [archivos de minivolcado](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="022a2-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="022a2-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>DETENER código</span><span class="sxs-lookup"><span data-stu-id="022a2-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="022a2-123">Código de error que identifica el error que detuvo la ejecución del kernel del sistema.</span><span class="sxs-lookup"><span data-stu-id="022a2-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="022a2-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="022a2-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="022a2-125">Todas las aplicaciones del sistema, los controladores y los archivos DLL se compilan de forma que la información de depuración reside en archivos independientes conocidos como archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="022a2-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="022a2-126">Por lo tanto, el sistema es más pequeño y más rápido, pero todavía se puede depurar si se instalan los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="022a2-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="022a2-127">Para obtener más información, vea [archivos de símbolos](symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="022a2-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="022a2-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modo de usuario</span><span class="sxs-lookup"><span data-stu-id="022a2-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="022a2-129">Modo de procesador en el que se ejecutan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="022a2-129">The processor mode in which applications run.</span></span> <span data-ttu-id="022a2-130">Hay un conjunto limitado de interfaces disponibles en este modo y el acceso a los datos del sistema es limitado.</span><span class="sxs-lookup"><span data-stu-id="022a2-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="022a2-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="022a2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="022a2-132">Configuración de la depuración automática</span><span class="sxs-lookup"><span data-stu-id="022a2-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



