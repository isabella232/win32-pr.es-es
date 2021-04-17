---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Habilitar la compatibilidad con Windows 7 para Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697736"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="54585-103">Habilitar la compatibilidad con Windows 7 para Intel AVX</span><span class="sxs-lookup"><span data-stu-id="54585-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="54585-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="54585-104">Affected Platforms</span></span>

 <span data-ttu-id="54585-105">**Clientes** : Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="54585-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="54585-106">**Servidores** : Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="54585-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="54585-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="54585-107">Feature Impact</span></span>

 <span data-ttu-id="54585-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="54585-108">**Severity** - Low</span></span>  
<span data-ttu-id="54585-109">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="54585-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="54585-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="54585-110">Description</span></span>

<span data-ttu-id="54585-111"><sup>¿Intel?</sup></span><span class="sxs-lookup"><span data-stu-id="54585-111">Intel<sup>?</sup></span></span> <span data-ttu-id="54585-112">Extensiones de vector avanzadas (AVX<sup>)</sup></span><span class="sxs-lookup"><span data-stu-id="54585-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="54585-113">es una extensión de vector de punto flotante de 256 bits SIMD de la arquitectura de Intel.</span><span class="sxs-lookup"><span data-stu-id="54585-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="54585-114">Incluye extensiones para los conjuntos de instrucciones y de registro.</span><span class="sxs-lookup"><span data-stu-id="54585-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="54585-115">Microsoft ha desarrollado algunas mejoras de API, como las funciones de XState, que permiten a las aplicaciones tener acceso y manipular la información y el estado de las características del procesador extendido, incluido AVX.</span><span class="sxs-lookup"><span data-stu-id="54585-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="54585-116">Escenarios de uso</span><span class="sxs-lookup"><span data-stu-id="54585-116">Usage Scenarios</span></span>

<span data-ttu-id="54585-117">Hay tres niveles generales de impacto potencial.</span><span class="sxs-lookup"><span data-stu-id="54585-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="54585-118">**Nivel 1:** Las aplicaciones que no usan directamente Intel AVX no verán ningún impacto en su funcionalidad, aunque llamen a bibliotecas o usen compiladores que utilicen o generen indirectamente extensiones de Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="54585-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="54585-119">Esto representa la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="54585-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="54585-120">**Nivel 2:** Las aplicaciones avanzadas que utilicen explícitamente el conjunto de instrucciones de Intel AVX podrán obtener acceso y cambiar el contenido del registro AVX cuando se produzca una excepción de hardware.</span><span class="sxs-lookup"><span data-stu-id="54585-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="54585-121">Una cantidad muy pequeña de aplicaciones estaría en esta categoría, ya que implica un conocimiento profundo de la secuencia de instrucciones que se ejecuta en el momento de la excepción, como las aplicaciones con secciones escritas en lenguaje ensamblador o las que generan código máquina en tiempo de ejecución (por ejemplo, los tiempos de ejecución de código administrado con la compilación Just-in-Time).</span><span class="sxs-lookup"><span data-stu-id="54585-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="54585-122">**Nivel 3:** Las aplicaciones del depurador podrán obtener acceso y manipular el estado AVX en la aplicación que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="54585-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="54585-123">Cómo aprovechar las funcionalidades de características</span><span class="sxs-lookup"><span data-stu-id="54585-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="54585-124">**Nivel 1:** No es necesario realizar ninguna acción para que las aplicaciones usen Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="54585-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="54585-125">**Nivel 2:** Las aplicaciones de esta categoría tienen la opción de obtener acceso y manipular el estado AVX en el momento de la excepción desde los filtros de excepciones.</span><span class="sxs-lookup"><span data-stu-id="54585-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="54585-126">Después de obtener el contexto del procesador base a través de GetExceptionInformation, los filtros deben:</span><span class="sxs-lookup"><span data-stu-id="54585-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="54585-127">**1.** Compruebe el valor de la **marca \_ XSTATE de contexto** .</span><span class="sxs-lookup"><span data-stu-id="54585-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="54585-128">Esta marca indica la presencia de al menos una característica XState en el contexto.</span><span class="sxs-lookup"><span data-stu-id="54585-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="54585-129">**2.** si este es el caso, llame a **GetXStateFeaturesMask** y pruebe el valor de la marca **XSTATE \_ AVX** en la máscara devuelta.</span><span class="sxs-lookup"><span data-stu-id="54585-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="54585-130">Esto indica la presencia del estado AVX en el contexto.</span><span class="sxs-lookup"><span data-stu-id="54585-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="54585-131">**3.** llame a **LocateXStateFeature** para recuperar la ubicación real en la que se almacena el estado AVX.</span><span class="sxs-lookup"><span data-stu-id="54585-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="54585-132">**Nivel 3:** No es necesario actualizar las aplicaciones del depurador existentes a menos que quieran acceder a los registros AVX de Intel:</span><span class="sxs-lookup"><span data-stu-id="54585-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="54585-133">**1.** para determinar si AVX está habilitado, el depurador debe usar:</span><span class="sxs-lookup"><span data-stu-id="54585-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="54585-134">GetEnabledXStateFeatures para obtener una máscara de las características habilitadas de XState en procesadores x86 o x64 con el fin de determinar qué características están presentes y habilitadas en el sistema antes de usar una característica de procesador XState o intentar manipular contextos XState</span><span class="sxs-lookup"><span data-stu-id="54585-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="54585-135">**2.** si AVX está presente y desea recuperar y manipular el estado AVX desde la aplicación que se está depurando (por ejemplo, GetThreadContext y SetThreadContext), el depurador debe usar:</span><span class="sxs-lookup"><span data-stu-id="54585-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="54585-136">Función InitializeContext para inicializar una estructura de contexto dentro de un búfer con el tamaño y la alineación necesarios</span><span class="sxs-lookup"><span data-stu-id="54585-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="54585-137">Función CopyContext para copiar una estructura de contexto de origen (incluido cualquier XState) en una estructura de contexto de destino inicializada</span><span class="sxs-lookup"><span data-stu-id="54585-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="54585-138">**3.** para probar, establecer y ubicar el estado AVX en un contexto de procesador, el depurador debe usar:</span><span class="sxs-lookup"><span data-stu-id="54585-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="54585-139">LocateXStateFeature para recuperar un puntero al estado del procesador para una característica XState individual dentro de una estructura de contexto</span><span class="sxs-lookup"><span data-stu-id="54585-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="54585-140">GetXStateFeaturesMask para devolver la máscara de las características de XState establecidas en una estructura de contexto</span><span class="sxs-lookup"><span data-stu-id="54585-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="54585-141">SetXStateFeaturesMask para establecer la máscara de las características de XState establecidas en una estructura de contexto</span><span class="sxs-lookup"><span data-stu-id="54585-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="54585-142">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="54585-142">Links to Other Resources</span></span>

-   <span data-ttu-id="54585-143">Para obtener información sobre las funciones de XState en el Windows SDK, vea [depurar funciones](../debug/debugging-functions.md).</span><span class="sxs-lookup"><span data-stu-id="54585-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="54585-144">Para obtener información general sobre las instrucciones y capacidades de Intel AVX, consulte [Intel AVX: nuevas fronteras en mejoras de rendimiento y eficiencia energética](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="54585-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
