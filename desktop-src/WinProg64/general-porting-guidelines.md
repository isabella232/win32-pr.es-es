---
title: Instrucciones generales de portabilidad
description: La migración de aplicaciones de 32 bits a Microsoft Windows de 64 bits será más fácil que la migración de aplicaciones de 16 bits a Windows de 32 bits. Sin embargo, el cambio se realizará de forma más fluida con cierta planeación cuidadosa. A continuación se muestran algunas directrices generales.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- trasladar aplicaciones de 32 bits a la programación de Windows de Windows 64 de 64 bits
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, directrices de migración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "104279732"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="8c5c7-107">Instrucciones generales de portabilidad</span><span class="sxs-lookup"><span data-stu-id="8c5c7-107">General Porting Guidelines</span></span>

<span data-ttu-id="8c5c7-108">La migración de aplicaciones de 32 bits a Microsoft Windows de 64 bits será más fácil que la migración de aplicaciones de 16 bits a Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="8c5c7-109">Sin embargo, el cambio se realizará de forma más fluida con cierta planeación cuidadosa.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="8c5c7-110">A continuación se muestran algunas directrices generales.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="8c5c7-111">Planificación</span><span class="sxs-lookup"><span data-stu-id="8c5c7-111">Planning</span></span>

-   <span data-ttu-id="8c5c7-112">Determinar la magnitud del esfuerzo necesario para el puerto.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="8c5c7-113">Mida la cantidad de trabajo que implica la identificación de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8c5c7-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="8c5c7-114">Problema 32: código de bit.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-114">Problem 32-bit code.</span></span> <span data-ttu-id="8c5c7-115">Compile el código de 32 bits con el compilador de 64 bits y examine la extensión de los errores y las advertencias.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="8c5c7-116">Componentes compartidos o dependencias.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-116">Shared components or dependencies.</span></span> <span data-ttu-id="8c5c7-117">Determine qué componentes de la aplicación se originan en otros equipos y si esos equipos planean desarrollar versiones de 64 bits de su código.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="8c5c7-118">Código de ensamblado o heredado.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-118">Legacy or assembly code.</span></span> <span data-ttu-id="8c5c7-119">las aplicaciones basadas en Windows de 16 bits no se ejecutan en Windows de 64 bits y se deben volver a escribir.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="8c5c7-120">Aunque el código de ensamblado x86 se ejecuta en WOW64, puede que desee volver a escribir este código para aprovechar la velocidad de la arquitectura Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="8c5c7-121">Porte toda la aplicación, no solo partes de ella.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="8c5c7-122">Aunque es posible migrar partes de una aplicación o limitar el código a 2G con/LARGEADDRESSAWARE: NO, esta estrategia negocia la ganancia a corto plazo para el dolor a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="8c5c7-123">/LARGEADDRESSAWARE: NO se omite para un binario ARM64.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="8c5c7-124">Busque sustitutos para las tecnologías que no se van a migrar.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="8c5c7-125">Algunas tecnologías, como DAO (objeto de acceso a datos) y el motor de base de datos de jet red, no se trasladarán a Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="8c5c7-126">Trate la versión de 64 bits como una versión de producto independiente.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="8c5c7-127">Aunque el producto de 64 bits puede compartir el mismo código base que el de 32 bits, necesita pruebas adicionales y puede tener otras consideraciones de la versión.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="8c5c7-128">Desarrollo</span><span class="sxs-lookup"><span data-stu-id="8c5c7-128">Development</span></span>

-   <span data-ttu-id="8c5c7-129">Comience a desarrollar código compatible ahora.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="8c5c7-130">Los desarrolladores pueden empezar a escribir código compatible con los archivos de encabezado de Windows más recientes y los nuevos tipos de datos sin efectos negativos en el desarrollo de productos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="8c5c7-131">Para obtener más información, consulte [preparación para Windows de 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="8c5c7-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="8c5c7-132">Asegúrese de que el código se puede compilar para Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="8c5c7-133">El nuevo modelo de datos se diseñó para permitir la creación de aplicaciones de 32 y 64 bits a partir de una única base de código con pocas modificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="8c5c7-134">Los equipos de desarrollo de SQL Server y Windows están desarrollando versiones de 32 y 64 bits de sus productos a partir de la misma base de código.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="8c5c7-135">Use las nuevas características de optimización del compilador para obtener el mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="8c5c7-136">La optimización del código para procesadores Intel Itanium es más importante que para x86.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="8c5c7-137">El compilador supone muchas de las funciones de optimización que el microprocesador ha controlado previamente.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="8c5c7-138">Puede maximizar el rendimiento de una aplicación de 64 bits con dos nuevas características de optimización del compilador: *optimización guiada por perfiles* y *optimización completa del programa*.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="8c5c7-139">Ambas características generan tiempos de compilación más prolongados y requieren el desarrollo temprano de Buenos escenarios de prueba.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="8c5c7-140">La *optimización guiada por perfiles* implica un proceso de compilación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="8c5c7-141">Durante la primera compilación, el código se instrumenta para capturar el comportamiento de ejecución.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="8c5c7-142">Esta información se utiliza durante la segunda compilación para guiar todas las características de optimización.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="8c5c7-143">La *optimización de todo el programa* analiza el código en todos los archivos de aplicación, no solo en uno único.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="8c5c7-144">Este enfoque aumenta el rendimiento de varias maneras, como una mejor inserción, así como el análisis de efectos secundarios mejorado y las convenciones de llamada personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="8c5c7-145">Prueba</span><span class="sxs-lookup"><span data-stu-id="8c5c7-145">Testing</span></span>

-   <span data-ttu-id="8c5c7-146">Determine si va a probar el código de 64 o 32 bits que se ejecuta en WOW64.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="8c5c7-147">Algunas aplicaciones incluyen código nativo de 64 bits y código de 32 bits que se ejecuta en WOW64.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="8c5c7-148">Investigue esto estrechamente durante el desarrollo de un plan de pruebas y decida si las herramientas de pruebas deben ser de 64 bits, de 32 bits o de combinación.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="8c5c7-149">A menudo, necesitará probar las versiones de 64 y 32 bits de su aplicación en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="8c5c7-150">Pruebe los componentes de 32 bits usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="8c5c7-151">En primer lugar, vuelva a compilar el código en 64 bits y pruebe.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="8c5c7-152">En segundo lugar, solucione los problemas, vuelva a compilar en 32 bits y, a continuación, pruebe.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="8c5c7-153">En tercer lugar, vuelva a compilar a 64 bits y test.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="8c5c7-154">Probar componentes COM y RPC.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="8c5c7-155">Asegúrese de que los componentes COM y RPC de 32 y 64 bits se comunican correctamente.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="8c5c7-156">También es posible que tenga que probar las comunicaciones con componentes de 16 bits a través de una red.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="8c5c7-157">Pruebe la versión de 32 bits en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="8c5c7-158">Los clientes pueden seguir usando aplicaciones de 32 bits en Windows de 64 bits, donde los problemas de rendimiento y de memoria no son consideraciones importantes.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="8c5c7-159">Pruebe diferentes configuraciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-159">Test different memory configurations.</span></span>

    <span data-ttu-id="8c5c7-160">Al agregar grandes cantidades de memoria en el servidor, a veces se exponen problemas no detectados anteriormente en la aplicación o en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8c5c7-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




