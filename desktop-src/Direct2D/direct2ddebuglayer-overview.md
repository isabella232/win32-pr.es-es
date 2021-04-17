---
title: Introducción a la capa de depuración de Direct2D
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656257"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="17236-103">Introducción a la capa de depuración de Direct2D</span><span class="sxs-lookup"><span data-stu-id="17236-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="17236-104">El nivel de depuración de Direct2D proporciona mensajes de depuración en tiempo de diseño para que pueda minimizar el error de aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="17236-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="17236-105">En esta información general se describen los conceptos básicos del nivel de depuración de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="17236-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="17236-106">Se supone que está familiarizado con la creación de aplicaciones básicas de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="17236-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="17236-107">Esta información general contiene las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="17236-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="17236-108">¿Qué es el nivel de depuración de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="17236-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="17236-109">Instalar la capa de depuración de Direct2D</span><span class="sxs-lookup"><span data-stu-id="17236-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="17236-110">Habilitar la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="17236-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="17236-111">Niveles de depuración</span><span class="sxs-lookup"><span data-stu-id="17236-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="17236-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17236-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="17236-113">¿Qué es el nivel de depuración de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="17236-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="17236-114">La capa de depuración de Direct2D, implementada de forma independiente de Direct2D en su propio archivo DLL denominado d2d1debug.dll, proporciona mensajes de depuración para que pueda usar con precisión las funciones de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="17236-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="17236-115">Los mensajes de depuración se suelen producir a causa de infracciones del contrato de API, como parámetros no válidos (pueden estar relacionados con Direct3D), recursos no válidos, infracciones de subprocesos y problemas de rendimiento como el uso de una capa cuando un clip sería suficiente.</span><span class="sxs-lookup"><span data-stu-id="17236-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="17236-116">Para especificar la cantidad de información de la que se realiza el seguimiento por la capa de depuración, puede especificar uno de los tres niveles de depuración: información, ADVERTENCIA y error. y un mensaje de error de nivel desencadena el punto de interrupción para ayudarle a depurar.</span><span class="sxs-lookup"><span data-stu-id="17236-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="17236-117">Instalar la capa de depuración de Direct2D</span><span class="sxs-lookup"><span data-stu-id="17236-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="17236-118">Para obtener instrucciones sobre cómo instalar la capa de depuración, vea [instalar la capa de depuración de Direct2D](installing-the-direct2d-debug-layer.md).</span><span class="sxs-lookup"><span data-stu-id="17236-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="17236-119">Habilitar la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="17236-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="17236-120">Para habilitar la capa de depuración en la aplicación, especifique un valor de [**\_ \_ nivel de depuración de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) distinto de **D2D1 \_ Debug \_ LEVEL \_ None** al crear un generador con la función [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="17236-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="17236-121">Si la capa de depuración de Direct2D está habilitada, el efecto de administración del color de Direct2D (CLSID \_ D2D1ColorManagement) puede producir una infracción de acceso al establecer un contexto de color.</span><span class="sxs-lookup"><span data-stu-id="17236-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="17236-122">La solución consiste en deshabilitar la capa de depuración cuando se usa el efecto administración del color</span><span class="sxs-lookup"><span data-stu-id="17236-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="17236-123">Habilitar la capa de depuración para un generador también habilita la información de depuración para cualquier objeto creado por ese generador.</span><span class="sxs-lookup"><span data-stu-id="17236-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="17236-124">En el ejemplo siguiente se habilita la capa de depuración para un generador cuando la aplicación se compila para la configuración de compilación de depuración.</span><span class="sxs-lookup"><span data-stu-id="17236-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="17236-125">Si no se especifican opciones de fábrica o se especifica un nivel de depuración "none", no se invoca la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="17236-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="17236-126">La capa de depuración nunca debe estar activa en la versión de lanzamiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="17236-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="17236-127">En la sección siguiente se describen los diferentes niveles de depuración definidos por la enumeración de [**\_ \_ nivel de depuración D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .</span><span class="sxs-lookup"><span data-stu-id="17236-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="17236-128">Niveles de depuración</span><span class="sxs-lookup"><span data-stu-id="17236-128">Debug Levels</span></span>

<span data-ttu-id="17236-129">La enumeración de [**\_ \_ nivel**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) de depuración D2D1 especifica tres niveles de depuración: error de depuración de D2D1 \_ \_ \_ (error), D2D1 de advertencia de nivel de depuración \_ \_ \_ (ADVERTENCIA) e \_ información de nivel de depuración D2D1 \_ \_ (información)</span><span class="sxs-lookup"><span data-stu-id="17236-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="17236-130">Estos niveles se interpretan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="17236-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="17236-131">**Error:** Direct2D envía mensajes de error graves a la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="17236-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="17236-132">Por ejemplo, si se interrumpe una restricción de subproceso, se producirá un error grave.</span><span class="sxs-lookup"><span data-stu-id="17236-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="17236-133">**ADVERTENCIA:** Direct2D envía mensajes de error y advertencias a la capa de depuración para que pueda tratar cualquiera de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="17236-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="17236-134">**Información:** Direct2D envía mensajes de error, advertencias e información de diagnóstico adicional a la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="17236-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="17236-135">Por ejemplo, los mensajes de mejora del rendimiento se enviarán en este nivel de depuración.</span><span class="sxs-lookup"><span data-stu-id="17236-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="17236-136">El valor de \_ nivel de depuración D2D1 \_ \_ ninguno (ninguno) indica que Direct2D no proporciona ningún resultado de depuración.</span><span class="sxs-lookup"><span data-stu-id="17236-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17236-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17236-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17236-138">Depurar mensajes</span><span class="sxs-lookup"><span data-stu-id="17236-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




