---
title: Introducción a la capa de depuración de Direct2D
description: Introducción a la capa de depuración de Direct2D
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833174e0d18b11e2384d838930d5508601cfceaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099993"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="2c3fe-103">Introducción a la capa de depuración de Direct2D</span><span class="sxs-lookup"><span data-stu-id="2c3fe-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="2c3fe-104">La capa de depuración de Direct2D proporciona mensajes de depuración en tiempo de diseño para minimizar los errores de la aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="2c3fe-105">En esta introducción se describen los conceptos básicos de la capa de depuración de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="2c3fe-106">Se supone que está familiarizado con la creación de aplicaciones básicas de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="2c3fe-107">Esta información general contiene las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="2c3fe-108">¿Qué es la capa de depuración de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="2c3fe-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="2c3fe-109">Instalación de la capa de depuración de Direct2D</span><span class="sxs-lookup"><span data-stu-id="2c3fe-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="2c3fe-110">Habilitación de la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="2c3fe-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="2c3fe-111">Niveles de depuración</span><span class="sxs-lookup"><span data-stu-id="2c3fe-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="2c3fe-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c3fe-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="2c3fe-113">¿Qué es la capa de depuración de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="2c3fe-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="2c3fe-114">La capa de depuración de Direct2D, implementada por separado de Direct2D en su propio archivo DLL denominado d2d1debug.dll, proporciona mensajes de depuración para permitirle usar con precisión las funciones de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="2c3fe-115">Los mensajes de depuración suelen ser el resultado de infracciones del contrato de API, como parámetros no válidos (podrían estar relacionados con Direct3D), recursos no válidos, infracciones de subprocesos y problemas de rendimiento, como el uso de una capa cuando bastaría con un clip.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="2c3fe-116">Para especificar la cantidad de información de la capa de depuración, puede especificar uno de los tres niveles de depuración: información, advertencia y error. y un mensaje de error de nivel desencadena el punto de interrupción para ayudarle a depurar.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="2c3fe-117">Instalación de la capa de depuración de Direct2D</span><span class="sxs-lookup"><span data-stu-id="2c3fe-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="2c3fe-118">Para obtener instrucciones sobre cómo instalar la capa de depuración, consulte [Instalación de la capa de depuración de Direct2D.](installing-the-direct2d-debug-layer.md)</span><span class="sxs-lookup"><span data-stu-id="2c3fe-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="2c3fe-119">Habilitación de la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="2c3fe-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="2c3fe-120">Para habilitar la capa de depuración en la aplicación, especifique un valor [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) distinto de **D2D1 \_ DEBUG LEVEL \_ \_ NONE** al crear un generador con la función [**D2D1CreateFactory.**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)</span><span class="sxs-lookup"><span data-stu-id="2c3fe-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="2c3fe-121">Si la capa de depuración de Direct2D está habilitada, el efecto de administración de colores de Direct2D (CLSID D2D1ColorManagement) puede provocar una infracción de acceso al establecer un contexto \_ de color.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="2c3fe-122">La solución alternativa consiste en deshabilitar la capa de depuración cuando se usa el efecto de administración de colores.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="2c3fe-123">La habilitación de la capa de depuración para un generador también habilita la información de depuración para cualquier objeto creado por ese generador.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="2c3fe-124">En el ejemplo siguiente se habilita la capa de depuración de un generador cuando la aplicación se compila para la configuración de compilación debug.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


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
> <span data-ttu-id="2c3fe-125">Si no se especifica ninguna opción de fábrica o se especifica un nivel de depuración de "none", no se invoca la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="2c3fe-126">La capa de depuración nunca debe estar activa en la versión de lanzamiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="2c3fe-127">En la sección siguiente se describen los distintos niveles de depuración definidos por la [**enumeración D2D1 \_ DEBUG \_ LEVEL.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)</span><span class="sxs-lookup"><span data-stu-id="2c3fe-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="2c3fe-128">Niveles de depuración</span><span class="sxs-lookup"><span data-stu-id="2c3fe-128">Debug Levels</span></span>

<span data-ttu-id="2c3fe-129">La enumeración [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) especifica tres niveles de depuración: D2D1 \_ DEBUG LEVEL ERROR \_ \_ (error), D2D1 \_ DEBUG LEVEL WARNING (advertencia) e \_ \_ D2D1 \_ DEBUG LEVEL INFORMATION \_ \_ (información).</span><span class="sxs-lookup"><span data-stu-id="2c3fe-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="2c3fe-130">Estos niveles se interpretan de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="2c3fe-131">**Error:** Direct2D envía mensajes de error graves a la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="2c3fe-132">Por ejemplo, la separación de una restricción de subprocesos generará un error grave.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="2c3fe-133">**Advertencia:** Direct2D envía mensajes de error y advertencias a la capa de depuración para que pueda abordar cualquiera de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="2c3fe-134">**Información:** Direct2D envía mensajes de error, advertencias e información de diagnóstico adicional a la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="2c3fe-135">Por ejemplo, los mensajes de mejora del rendimiento se enviarán en este nivel de depuración.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="2c3fe-136">El valor D2D1 DEBUG LEVEL NONE (none) indica que \_ \_ \_ Direct2D no proporciona ninguna salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c3fe-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c3fe-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c3fe-138">Depurar mensajes</span><span class="sxs-lookup"><span data-stu-id="2c3fe-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




