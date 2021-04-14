---
title: Información general de DWriteCore
description: DWriteCore es la implementación de la reunión del proyecto de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361806"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="0643f-105">Información general de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-105">DWriteCore overview</span></span>

<span data-ttu-id="0643f-106">DWriteCore es la implementación de la [reunión del proyecto](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="0643f-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md).</span></span> <span data-ttu-id="0643f-107">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="0643f-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="0643f-108">En este tema introductorio se describe qué es DWriteCore y se muestra cómo instalarlo en el entorno de desarrollo y programar con él.</span><span class="sxs-lookup"><span data-stu-id="0643f-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="0643f-109">La propuesta de valor de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="0643f-110">[DirectWrite](./direct-write-portal.md) es compatible con una amplia gama de características que lo convierte en la herramienta de representación de fuentes preferida en Windows para la mayoría de las aplicaciones &mdash; , ya sea a través de llamadas directas o a través de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="0643f-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="0643f-111">DirectWrite incluye un sistema de diseño de texto independiente del dispositivo, representación de texto de [Microsoft ClearType](/typography/cleartype/) de alta calidad, texto con aceleración de hardware, texto multiforma, características avanzadas de tipografía de [® OpenType](/typography/opentype/) , compatibilidad con idiomas amplio y diseño y representación compatibles con [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="0643f-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="0643f-112">DirectWrite ha estado disponible desde Windows Vista SP2 y ha evolucionado a lo largo de los años para incluir características más avanzadas, como fuentes variables, lo que permite a los desarrolladores aplicar estilos, pesos y otros atributos a una fuente con un solo recurso de fuente.</span><span class="sxs-lookup"><span data-stu-id="0643f-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="0643f-113">Debido a la larga duración de DirectWrite, sin embargo, los avances en el desarrollo han dado la idea de dejar versiones anteriores de Windows detrás.</span><span class="sxs-lookup"><span data-stu-id="0643f-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="0643f-114">Además, el estado de DirectWrite como la tecnología de representación de texto Premier solo está limitado a Windows, lo que deja que las aplicaciones multiplataforma escriban su propia pila de representación de texto o que se basen en soluciones de terceros.</span><span class="sxs-lookup"><span data-stu-id="0643f-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="0643f-115">DWriteCore resuelve los problemas fundamentales de la característica de versión huérfana y la compatibilidad entre plataformas mediante la eliminación de la biblioteca del sistema y el destino de todos los puntos de conexión admitidos.</span><span class="sxs-lookup"><span data-stu-id="0643f-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="0643f-116">Para ello, hemos integrado DWriteCore en la reunión de proyectos con una API pública que es compatible con todos los puntos de conexión de Windows hasta Windows 8 y abre la puerta para que la use entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="0643f-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="0643f-117">El valor principal que DWriteCore le proporciona, como desarrollador, en Project reunion es que proporciona acceso a todas las características de DirectWrite actuales hasta el nivel inferior a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0643f-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="0643f-118">Todas las características de DWriteCore funcionarán igual en todas las versiones de nivel inferior; en otras palabras, todas las características actuales funcionarán en Windows 8, 8,1 y todas las versiones de Windows 10, sin ninguna disparidad con respecto a las características que podrían funcionar en cada versión.</span><span class="sxs-lookup"><span data-stu-id="0643f-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="0643f-119">Aplicación de demostración de DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="0643f-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="0643f-120">DWriteCore se muestra por medio de la aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que ahora está disponible para su descarga y estudio.</span><span class="sxs-lookup"><span data-stu-id="0643f-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="0643f-121">Introducción a DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-121">Get started with DWriteCore</span></span>

<span data-ttu-id="0643f-122">En la versión preliminar de Project reunion 0,1, actualmente no se admite la instalación del paquete de NuGet de reunión del proyecto en sus propios proyectos.</span><span class="sxs-lookup"><span data-stu-id="0643f-122">For the Project Reunion 0.1 Prerelease, we currently don't support installing the Project Reunion NuGet package into your own projects.</span></span> <span data-ttu-id="0643f-123">En su lugar, la opción admitida actualmente para su propia programación con DWriteCore es comenzar con el proyecto de aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) y basar el desarrollo en ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="0643f-123">Instead, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span>

<span data-ttu-id="0643f-124">Después, puede quitar cualquier código fuente (o archivos) existente del proyecto de ejemplo y agregar cualquier nuevo código fuente (o archivos) al proyecto.</span><span class="sxs-lookup"><span data-stu-id="0643f-124">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span> <span data-ttu-id="0643f-125">Para obtener más información sobre la programación con DWriteCore, consulte la sección [programación con DWriteCore](#programming-with-dwritecore) más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="0643f-125">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="0643f-126">Fases de versión de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-126">The release phases of DWriteCore</span></span>

<span data-ttu-id="0643f-127">La migración de DirectWrite a DWriteCore es un proyecto suficientemente grande para abarcar varios ciclos de versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="0643f-127">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="0643f-128">Ese proyecto se divide en fases, cada una de las cuales corresponde a un fragmento de funcionalidad entregado en una versión.</span><span class="sxs-lookup"><span data-stu-id="0643f-128">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="0643f-129">Características de la versión actual de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-129">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="0643f-130">La versión de DWriteCore disponible actualmente contiene las herramientas básicas que usted, como desarrollador, necesitan para consumir DWriteCore, incluidas las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="0643f-130">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="0643f-131">Enumeración de fuentes.</span><span class="sxs-lookup"><span data-stu-id="0643f-131">Font enumeration.</span></span>
- <span data-ttu-id="0643f-132">API de fuentes.</span><span class="sxs-lookup"><span data-stu-id="0643f-132">Font API.</span></span>
- <span data-ttu-id="0643f-133">Forma.</span><span class="sxs-lookup"><span data-stu-id="0643f-133">Shaping.</span></span>
- <span data-ttu-id="0643f-134">API de representación de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="0643f-134">Low-level rendering APIs.</span></span> <span data-ttu-id="0643f-135">Esto es parcial en la fase actual &mdash; DWriteCore no interopera con [Direct2D](../direct2d/direct2d-portal.md), pero puede usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) y [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="0643f-135">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="0643f-136">Funcionalidad básica de diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="0643f-136">Basic text layout functionality.</span></span>
- <span data-ttu-id="0643f-137">API de representación de texto.</span><span class="sxs-lookup"><span data-stu-id="0643f-137">Text-rendering APIs.</span></span>
- <span data-ttu-id="0643f-138">Destino de representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="0643f-138">Bitmap render target.</span></span>
- <span data-ttu-id="0643f-139">Fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="0643f-139">Color fonts.</span></span>
- <span data-ttu-id="0643f-140">Optimizaciones misceláneas (limpieza de la caché de fuentes, cargador de fuentes en memoria, etc.).</span><span class="sxs-lookup"><span data-stu-id="0643f-140">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="0643f-141">La característica de pancarta en esta fase es fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="0643f-141">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="0643f-142">Las fuentes de color permiten representar las fuentes con una funcionalidad de color más sofisticada más allá de los simples colores sencillos.</span><span class="sxs-lookup"><span data-stu-id="0643f-142">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="0643f-143">Por ejemplo, las fuentes de color son lo que impulsa la capacidad de representar las fuentes de Emoji y de los iconos de la barra de herramientas (por ejemplo, la última usada por Office).</span><span class="sxs-lookup"><span data-stu-id="0643f-143">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="0643f-144">Las fuentes de color se introdujeron por primera vez en Windows 8.1, pero la característica se amplió mucho en Windows 10, versión 1607 (actualización de aniversario).</span><span class="sxs-lookup"><span data-stu-id="0643f-144">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="0643f-145">El trabajo de limpieza de la memoria caché de fuentes y el cargador de fuentes en memoria permiten una carga más rápida de fuentes y mejoras en la memoria.</span><span class="sxs-lookup"><span data-stu-id="0643f-145">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="0643f-146">Con estas características, puede empezar a aprovechar de inmediato algunas de las funcionalidades de núcleo moderno de DirectWrite, como las &mdash; fuentes variables de &mdash; nivel inferior a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0643f-146">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="0643f-147">Esta iteración de la biblioteca también se puede consumir en [Android](https://www.android.com/)y **Linux**.</span><span class="sxs-lookup"><span data-stu-id="0643f-147">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="0643f-148">Las fuentes variables son una de las características más importantes para los clientes de DirectWrite; se introdujeron en Windows 10, versión 1709 (Fall Creators Update), por lo que tener acceso a ellos en versiones anteriores es una gran ayuda como desarrollador.</span><span class="sxs-lookup"><span data-stu-id="0643f-148">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="0643f-149">Nuestra invitación a usted como desarrollador de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0643f-149">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="0643f-150">DWriteCore, junto con otros componentes de la reunión del proyecto, se desarrollarán con la apertura de los comentarios de los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="0643f-150">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="0643f-151">Le invitamos a empezar a explorar DWriteCore y a proporcionar información o solicitudes en el desarrollo de características en nuestro [repositorio de github](https://github.com/microsoft/ProjectReunion/)de la Unión del proyecto.</span><span class="sxs-lookup"><span data-stu-id="0643f-151">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="0643f-152">Programar con DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-152">Programming with DWriteCore</span></span>

<span data-ttu-id="0643f-153">Como ya se mencionó, para la versión preliminar del proyecto reunion 0,1, la opción admitida actualmente para su propia programación con DWriteCore es comenzar con el proyecto de aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="0643f-153">As already mentioned, for the Project Reunion 0.1 Prerelease, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project.</span></span>

<span data-ttu-id="0643f-154">Al igual que con [DirectWrite](./direct-write-portal.md), puede programar con DWriteCore a través de su API de com-Light, a través de la interfaz [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="0643f-154">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="0643f-155">**DWriteCoreGallery** ya incluye el `dwrite_core.h` archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="0643f-155">**DWriteCoreGallery** already includes the `dwrite_core.h` header file.</span></span> <span data-ttu-id="0643f-156">Dicho encabezado define primero el token *DWRITE_CORE* y, a continuación, lo incluye `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="0643f-156">That header first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="0643f-157">El token *DWRITE_CORE* es importante, ya que dirige los encabezados incluidos posteriormente para que todas las API de DirectWrite estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="0643f-157">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="0643f-158">Una vez incluido un proyecto `dwrite_core.h` , puede continuar y escribir código, compilar y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="0643f-158">Once a project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="0643f-159">API nuevas o diferentes para DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0643f-159">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="0643f-160">La superficie de la API de DWriteCore es lo más grande que para [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="0643f-160">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="0643f-161">Pero hay un pequeño número de API nuevas que solo están en DWriteCore en el momento actual.</span><span class="sxs-lookup"><span data-stu-id="0643f-161">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="0643f-162">Crear un objeto de generador restringido</span><span class="sxs-lookup"><span data-stu-id="0643f-162">Create a restricted factory object</span></span>

<span data-ttu-id="0643f-163">La enumeración [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) tiene una nueva constante &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="0643f-163">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_RESTRICTED**.</span></span> <span data-ttu-id="0643f-164">Un generador restringido está más bloqueado que un generador aislado.</span><span class="sxs-lookup"><span data-stu-id="0643f-164">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="0643f-165">No interactúa de ningún modo con una memoria caché de fuentes entre procesos ni persistentes.</span><span class="sxs-lookup"><span data-stu-id="0643f-165">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="0643f-166">Además, la colección de fuentes del sistema devuelta desde este generador solo incluye fuentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="0643f-166">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="0643f-167">Aquí se muestra cómo se puede usar **DWRITE_FACTORY_TYPE_RESTRICTED** para crear un objeto de generador restringido cuando se llama a la función Free de [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="0643f-167">Here's how you can use **DWRITE_FACTORY_TYPE_RESTRICTED** to create a restricted factory object when you call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="0643f-168">Si pasa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versión anterior de DirectWrite que no lo admite, **DWriteCreateFactory** devuelve **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="0643f-168">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="0643f-169">Dibujar glifos en un mapa de bits de memoria del sistema</span><span class="sxs-lookup"><span data-stu-id="0643f-169">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="0643f-170">DirectWrite tiene una interfaz de destino de representación de mapas de bits que admite la representación de glifos en un mapa de bits en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="0643f-170">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="0643f-171">Sin embargo, actualmente, la única manera de obtener acceso a los datos de píxeles subyacentes es pasar a través de GDI, por lo que la API no se puede usar entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="0643f-171">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="0643f-172">Esto se soluciona fácilmente agregando un método para recuperar los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0643f-172">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="0643f-173">Por lo tanto, DWriteCore introduce la interfaz [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) y su método [**IDWriteBitmapRenderTarget2:: GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="0643f-173">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="0643f-174">Ese método toma un parámetro de tipo (puntero a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que es un nuevo struct.</span><span class="sxs-lookup"><span data-stu-id="0643f-174">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="0643f-175">La aplicación crea un destino de representación de mapa de bits llamando a [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="0643f-175">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="0643f-176">En Windows, un destino de representación de mapas de bits encapsula un DC de memoria de GDI con un mapa de bits independiente del dispositivo GDI (DIB) seleccionado en él.</span><span class="sxs-lookup"><span data-stu-id="0643f-176">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="0643f-177">[IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) representa glifos en el Dib.</span><span class="sxs-lookup"><span data-stu-id="0643f-177">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="0643f-178">DirectWrite representa los glifos en sí sin pasar por GDI.</span><span class="sxs-lookup"><span data-stu-id="0643f-178">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="0643f-179">A continuación, la aplicación puede obtener la **HDC** del destino de representación del mapa de bits y usar [bitblt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar los píxeles en una ventana **HDC**.</span><span class="sxs-lookup"><span data-stu-id="0643f-179">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="0643f-180">En plataformas que no son de Windows, la aplicación puede seguir creando un destino de representación de mapa de bits, pero simplemente encapsula una matriz de memoria del sistema sin **HDC** y sin Dib.</span><span class="sxs-lookup"><span data-stu-id="0643f-180">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="0643f-181">Sin una **HDC**, debe haber otra manera de que la aplicación obtenga los píxeles del mapa de bits para que pueda copiarlos, o bien usarlos.</span><span class="sxs-lookup"><span data-stu-id="0643f-181">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="0643f-182">Incluso en Windows, a veces resulta útil obtener los datos de píxeles reales y se muestra la manera actual de hacerlo en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="0643f-182">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="0643f-183">Otras diferencias de API entre DWriteCore y DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0643f-183">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="0643f-184">Hay algunas API que son solo códigos auxiliares o que se comportan de manera ligeramente diferente en plataformas que no son de Windows.</span><span class="sxs-lookup"><span data-stu-id="0643f-184">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="0643f-185">Por ejemplo, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) devuelve **E_NOTIMPL** en plataformas que no son de Windows, ya que no hay nada como **HDC** sin [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="0643f-185">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="0643f-186">Y, por último, hay algunas otras API de Windows que se suelen usar junto con DirectWrite (Direct2D es un ejemplo importante).</span><span class="sxs-lookup"><span data-stu-id="0643f-186">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="0643f-187">Sin embargo, actualmente, Direct2D y DWriteCore no interoperan.</span><span class="sxs-lookup"><span data-stu-id="0643f-187">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="0643f-188">Por ejemplo, si crea un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) con DWriteCore y lo pasa a [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), se producirá un error en esa llamada.</span><span class="sxs-lookup"><span data-stu-id="0643f-188">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>