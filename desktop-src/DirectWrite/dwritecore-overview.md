---
title: Información general de DWriteCore
description: DWriteCore es la implementación project-project de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 9e0bc6cf6433f65fa1bc28ec2654492057842b94
ms.sourcegitcommit: 5a39ee31075cd81ab865c81c39e128b8312da21b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "110207387"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="a45aa-105">Información general de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-105">DWriteCore overview</span></span>

<span data-ttu-id="a45aa-106">DWriteCore es la implementación [project- and-project de](/windows/apps/project-reunion/) [DirectWrite](./direct-write-portal.md) (DirectWrite es la API de DirectX para la representación de texto de alta calidad, fuentes de esquema independientes de la resolución y compatibilidad completa con texto Unicode y diseño).</span><span class="sxs-lookup"><span data-stu-id="a45aa-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="a45aa-107">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 10, versión 1809 (10.0; Compilación 17763) y abre la puerta para que la use multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="a45aa-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="a45aa-108">En este tema introductorio se describe qué es DWriteCore y se muestra cómo instalarlo en el entorno de desarrollo y programar con él.</span><span class="sxs-lookup"><span data-stu-id="a45aa-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="a45aa-109">La propuesta de valor de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="a45aa-110">[DirectWrite](./direct-write-portal.md) admite una amplia gama de características que la convierten en la herramienta de representación de fuentes preferida en Windows para la mayoría de las aplicaciones, ya sea a través de llamadas directas o a través de &mdash; [Direct2D.](../direct2d/direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="a45aa-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="a45aa-111">DirectWrite incluye un sistema de diseño de texto independiente del dispositivo, representación de texto [Microsoft ClearType](/typography/cleartype/) de subpíxeles de alta calidad, texto acelerado por hardware, texto multi format, características avanzadas de [tipografía OpenType®](/typography/opentype/) compatibilidad con lenguaje ancho y diseño y representación compatibles con [GDI.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="a45aa-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="a45aa-112">DirectWrite ha estado disponible desde Windows Vista SP2 y ha evolucionado a lo largo de los años para incluir características más avanzadas, como fuentes variables, que le permiten aplicar estilos, pesos y otros atributos a una fuente con un solo recurso de fuente.</span><span class="sxs-lookup"><span data-stu-id="a45aa-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="a45aa-113">Sin embargo, debido a la larga duración de DirectWrite, los avances en el desarrollo han tendido a dejar atrás las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="a45aa-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="a45aa-114">Además, el estado de DirectWrite como tecnología de representación de texto premier solo se limita a Windows, lo que deja que las aplicaciones multiplataforma escriban su propia pila de representación de texto o se basen en soluciones de terceros.</span><span class="sxs-lookup"><span data-stu-id="a45aa-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="a45aa-115">DWriteCore resuelve los problemas fundamentales de la característica de versión huérfana y la compatibilidad multiplataforma mediante la eliminación de la biblioteca del sistema y el destino de todos los posibles puntos de conexión admitidos.</span><span class="sxs-lookup"><span data-stu-id="a45aa-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="a45aa-116">Con ese fin, hemos integrado DWriteCore en Project Hacer.</span><span class="sxs-lookup"><span data-stu-id="a45aa-116">To that end, we've integrated DWriteCore into Project Reunion.</span></span>

<span data-ttu-id="a45aa-117">El valor principal que DWriteCore le proporciona, como desarrollador, en Project Hacer es que proporciona acceso a muchas (y, finalmente, a todas) características de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="a45aa-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="a45aa-118">Todas las características de DWriteCore funcionarán igual en todas las versiones de nivel inferior sin ninguna disparidad con respecto a qué características pueden funcionar en qué versiones.</span><span class="sxs-lookup"><span data-stu-id="a45aa-118">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="a45aa-119">La aplicación de demostración DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="a45aa-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="a45aa-120">DWriteCore se muestra a través de la aplicación de ejemplo [DWriteCoreGallery,](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) que ahora está disponible para su descarga y estudio.</span><span class="sxs-lookup"><span data-stu-id="a45aa-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="a45aa-121">Introducción a DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-121">Get started with DWriteCore</span></span>

<span data-ttu-id="a45aa-122">DWriteCore forma parte de [Project Project Project 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)</span><span class="sxs-lookup"><span data-stu-id="a45aa-122">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="a45aa-123">En esta sección se describe cómo configurar el entorno de desarrollo para la programación con DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="a45aa-123">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="a45aa-124">Instalación del VSIX project-in-project 0.5</span><span class="sxs-lookup"><span data-stu-id="a45aa-124">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="a45aa-125">En Visual Studio, haga clic en **Extensiones**  >  **Administrar** extensiones, busque Project Project *y* descargue la extensión Project Extension.</span><span class="sxs-lookup"><span data-stu-id="a45aa-125">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="a45aa-126">Cierre y vuelva a Visual Studio y siga las indicaciones para instalar la extensión.</span><span class="sxs-lookup"><span data-stu-id="a45aa-126">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="a45aa-127">Para obtener más información, [vea Project Project 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)y [Set up your development environment (for Project Project) (Configurar el](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment)entorno de desarrollo (para Project Project).</span><span class="sxs-lookup"><span data-stu-id="a45aa-127">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Set up your development environment (for Project Reunion)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="a45aa-128">Creación de un nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="a45aa-128">Create a new project</span></span>

<span data-ttu-id="a45aa-129">En Visual Studio, cree un proyecto a partir de la plantilla de proyecto Aplicación vacía **empaquetada (WinUI 3 en** escritorio).</span><span class="sxs-lookup"><span data-stu-id="a45aa-129">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="a45aa-130">Puede encontrar esa plantilla de proyecto eligiendo el lenguaje: *C++*; platform: *ProjectPlata;* Tipo de proyecto: *Escritorio.*</span><span class="sxs-lookup"><span data-stu-id="a45aa-130">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="a45aa-131">Para obtener más información, consulta [Introducción a WinUI 3 para aplicaciones de escritorio.](/windows/apps/winui/winui3/get-started-winui3-for-desktop)</span><span class="sxs-lookup"><span data-stu-id="a45aa-131">For more info, see [Get started with WinUI 3 for desktop apps](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="a45aa-132">Instalación del paquete NuGet Microsoft.ProjectReunion.DWrite</span><span class="sxs-lookup"><span data-stu-id="a45aa-132">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="a45aa-133">En Visual Studio, haga  clic en Project Manage NuGet Packages... Browse (Administrar proyectos paquetes NuGet... Examinar), escriba o pegue \>  \>  **Microsoft.ProjectReunion.DWrite**  en el cuadro de búsqueda, seleccione el elemento en los resultados de la búsqueda y, a continuación, haga clic en Instalar para instalar el paquete para ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="a45aa-133">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="a45aa-134">Como alternativa, comience con la aplicación de ejemplo DWriteCoreGallery.</span><span class="sxs-lookup"><span data-stu-id="a45aa-134">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="a45aa-135">Como alternativa, puede programar con DWriteCore empezando por el proyecto de aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) y basar el desarrollo en ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="a45aa-135">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="a45aa-136">A continuación, puede quitar cualquier código fuente existente (o archivos) de ese proyecto de ejemplo y agregar cualquier nuevo código fuente (o archivos) al proyecto.</span><span class="sxs-lookup"><span data-stu-id="a45aa-136">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="a45aa-137">Uso de DWriteCore en el proyecto</span><span class="sxs-lookup"><span data-stu-id="a45aa-137">Use DWriteCore in your project</span></span>

<span data-ttu-id="a45aa-138">Para obtener más información sobre la programación con DWriteCore, vea la sección Programming with DWriteCore (Programación con [DWriteCore)](#programming-with-dwritecore) más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="a45aa-138">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="a45aa-139">Fases de lanzamiento de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-139">The release phases of DWriteCore</span></span>

<span data-ttu-id="a45aa-140">La porción de DirectWrite a DWriteCore es un proyecto lo suficientemente grande como para abarcar varios ciclos de versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="a45aa-140">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="a45aa-141">Ese proyecto se divide en fases, cada una de las cuales corresponde a un fragmento de funcionalidad entregado en una versión.</span><span class="sxs-lookup"><span data-stu-id="a45aa-141">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="a45aa-142">Características de la versión actual de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-142">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="a45aa-143">La versión de DWriteCore disponible actualmente forma parte de [Project Hacer 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)</span><span class="sxs-lookup"><span data-stu-id="a45aa-143">The version of DWriteCore currently available is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="a45aa-144">Contiene las herramientas básicas que, como desarrollador, necesita para consumir DWriteCore, incluidas las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="a45aa-144">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="a45aa-145">Enumeración de fuentes.</span><span class="sxs-lookup"><span data-stu-id="a45aa-145">Font enumeration.</span></span>
- <span data-ttu-id="a45aa-146">API de fuente.</span><span class="sxs-lookup"><span data-stu-id="a45aa-146">Font API.</span></span>
- <span data-ttu-id="a45aa-147">Formar.</span><span class="sxs-lookup"><span data-stu-id="a45aa-147">Shaping.</span></span>
- <span data-ttu-id="a45aa-148">API de representación de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="a45aa-148">Low-level rendering APIs.</span></span> <span data-ttu-id="a45aa-149">Esto es parcial en la fase actual DWriteCore no interopera con &mdash; [Direct2D,](../direct2d/direct2d-portal.md)pero puede usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)</span><span class="sxs-lookup"><span data-stu-id="a45aa-149">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="a45aa-150">Funcionalidad básica de diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="a45aa-150">Basic text layout functionality.</span></span>
- <span data-ttu-id="a45aa-151">API de representación de texto.</span><span class="sxs-lookup"><span data-stu-id="a45aa-151">Text-rendering APIs.</span></span>
- <span data-ttu-id="a45aa-152">Destino de representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a45aa-152">Bitmap render target.</span></span>
- <span data-ttu-id="a45aa-153">Fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="a45aa-153">Color fonts.</span></span>
- <span data-ttu-id="a45aa-154">Optimizaciones misceláneas (limpieza de la caché de fuentes, cargador de fuentes en memoria, entre otras).</span><span class="sxs-lookup"><span data-stu-id="a45aa-154">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="a45aa-155">Una característica de banner son las fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="a45aa-155">A banner feature is color fonts.</span></span> <span data-ttu-id="a45aa-156">Las fuentes de color permiten representar las fuentes con una funcionalidad de color más sofisticada más allá de los colores simples.</span><span class="sxs-lookup"><span data-stu-id="a45aa-156">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="a45aa-157">Por ejemplo, las fuentes de color son lo que potencia la capacidad de representar fuentes de icono de emoji y de barra de herramientas (la última de las cuales la usa Office, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="a45aa-157">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="a45aa-158">Las fuentes de color se introdujeron por primera vez en Windows 8.1, pero la característica se expandió en gran medida en Windows 10, versión 1607 (Actualización de aniversario).</span><span class="sxs-lookup"><span data-stu-id="a45aa-158">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="a45aa-159">El trabajo de limpieza de la caché de fuentes y del cargador de fuentes en memoria permite una carga más rápida de fuentes y mejoras en la memoria.</span><span class="sxs-lookup"><span data-stu-id="a45aa-159">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="a45aa-160">Con estas características, puede empezar a aprovechar inmediatamente algunas de las funcionalidades básicas modernas de DirectWrite, &mdash; como las fuentes variables.</span><span class="sxs-lookup"><span data-stu-id="a45aa-160">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="a45aa-161">Las fuentes variables son una de las características más importantes para los clientes de DirectWrite. se introdujeron en Windows 10, versión 1709 (Fall Creators Update), por lo que acceder a ellos en versiones anteriores es una ventaja importante para usted como desarrollador.</span><span class="sxs-lookup"><span data-stu-id="a45aa-161">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a significant benefit to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="a45aa-162">Nuestra invitación para usted como desarrollador de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a45aa-162">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="a45aa-163">DWriteCore, junto con otros componentes project project, se desarrollará con apertura a los comentarios de los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="a45aa-163">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="a45aa-164">Le invitamos a empezar a explorar DWriteCore y a proporcionar información o solicitudes sobre el desarrollo de características en nuestro repositorio de [GitHub Project GitHub.](https://github.com/microsoft/ProjectReunion/)</span><span class="sxs-lookup"><span data-stu-id="a45aa-164">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="a45aa-165">Programación con DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-165">Programming with DWriteCore</span></span>

<span data-ttu-id="a45aa-166">Al igual que [con DirectWrite,](./direct-write-portal.md)programe con DWriteCore a través de su API DE LUZ COM, a través de la [**interfaz IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)</span><span class="sxs-lookup"><span data-stu-id="a45aa-166">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="a45aa-167">Para usar DWriteCore, es necesario incluir el archivo `dwrite_core.h` de encabezado.</span><span class="sxs-lookup"><span data-stu-id="a45aa-167">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="a45aa-168">El `dwrite_core.h` archivo de encabezado define primero el token *DWRITE_CORE* y, a continuación, incluye el archivo `dwrite_3.h` de encabezado.</span><span class="sxs-lookup"><span data-stu-id="a45aa-168">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="a45aa-169">El *DWRITE_CORE* es importante, ya que dirige los encabezados incluidos posteriormente para que todas las API de DirectWrite estén disponibles para usted.</span><span class="sxs-lookup"><span data-stu-id="a45aa-169">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="a45aa-170">Una vez que el proyecto haya `dwrite_core.h` incluido , puede continuar y escribir código, compilar y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a45aa-170">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="a45aa-171">API nuevas o diferentes para DWriteCore</span><span class="sxs-lookup"><span data-stu-id="a45aa-171">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="a45aa-172">La superficie de la API DWriteCore es prácticamente la misma que para [DirectWrite.](/windows/win32/api/_directwrite/)</span><span class="sxs-lookup"><span data-stu-id="a45aa-172">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="a45aa-173">Pero hay un pequeño número de nuevas API que solo están en DWriteCore en la actualidad.</span><span class="sxs-lookup"><span data-stu-id="a45aa-173">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="a45aa-174">Creación de un objeto de generador</span><span class="sxs-lookup"><span data-stu-id="a45aa-174">Create a factory object</span></span>

<span data-ttu-id="a45aa-175">La [**función gratuita DWriteCoreCreateFactory**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) crea un objeto de generador que se usa para la posterior creación de objetos DWriteCore individuales.</span><span class="sxs-lookup"><span data-stu-id="a45aa-175">The [**DWriteCoreCreateFactory**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="a45aa-176">**DWriteCoreCreateFactory es** funcionalmente igual que la función [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada por la versión del sistema de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="a45aa-176">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="a45aa-177">La función DWriteCore tiene un nombre diferente para evitar ambigüedades.</span><span class="sxs-lookup"><span data-stu-id="a45aa-177">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="a45aa-178">Creación de un objeto de generador restringido</span><span class="sxs-lookup"><span data-stu-id="a45aa-178">Create a restricted factory object</span></span>

<span data-ttu-id="a45aa-179">La [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeración tiene una nueva &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, que indica un generador restringido.</span><span class="sxs-lookup"><span data-stu-id="a45aa-179">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="a45aa-180">Una fábrica restringida está más bloqueada que una factoría aislada.</span><span class="sxs-lookup"><span data-stu-id="a45aa-180">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="a45aa-181">No interactúa con una caché de fuentes persistente ni entre procesos de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="a45aa-181">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="a45aa-182">Además, la colección de fuentes del sistema devuelta desde este generador incluye solo fuentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="a45aa-182">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="a45aa-183">Aquí se muestra cómo puede usar **DWRITE_FACTORY_TYPE_ISOLATED2** para crear un objeto de generador restringido al llamar a la función [**gratuita DWriteCoreCreateFactory.**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory)</span><span class="sxs-lookup"><span data-stu-id="a45aa-183">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="a45aa-184">Si pasa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versión anterior de DirectWrite que no la **admite,** **DWriteCreateFactory** devuelve E_INVALIDARG .</span><span class="sxs-lookup"><span data-stu-id="a45aa-184">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="a45aa-185">Dibujar glifos en un mapa de bits de memoria del sistema</span><span class="sxs-lookup"><span data-stu-id="a45aa-185">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="a45aa-186">DirectWrite tiene una interfaz de destino de representación de mapa de bits que admite la representación de glifos en un mapa de bits en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="a45aa-186">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="a45aa-187">Sin embargo, actualmente la única manera de obtener acceso a los datos de píxel subyacente es pasar por GDI, por lo que la API no se puede usar entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="a45aa-187">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="a45aa-188">Esto se corrige fácilmente mediante la adición de un método para recuperar los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a45aa-188">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="a45aa-189">Por lo tanto, DWriteCore presenta la interfaz [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) y su método [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="a45aa-189">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="a45aa-190">Ese método toma un parámetro de tipo (puntero a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que es un nuevo struct.</span><span class="sxs-lookup"><span data-stu-id="a45aa-190">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="a45aa-191">La aplicación crea un destino de representación de mapa de bits mediante una [llamada a IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="a45aa-191">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="a45aa-192">En Windows, un destino de representación de mapa de bits encapsula un controlador de dominio de memoria GDI con un mapa de bits independiente del dispositivo GDI (DIB) seleccionado en él.</span><span class="sxs-lookup"><span data-stu-id="a45aa-192">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="a45aa-193">[IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) representa glifos en la DIB.</span><span class="sxs-lookup"><span data-stu-id="a45aa-193">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="a45aa-194">DirectWrite representa los glifos sin pasar por GDI.</span><span class="sxs-lookup"><span data-stu-id="a45aa-194">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="a45aa-195">A continuación, la aplicación puede obtener **el HDC** del destino de representación de mapa de bits y usar [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar los píxeles en una ventana **HDC**.</span><span class="sxs-lookup"><span data-stu-id="a45aa-195">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="a45aa-196">En plataformas que no son de Windows, la aplicación todavía puede crear un destino de representación de mapa de bits, pero simplemente encapsula una matriz de memoria del sistema sin **HDC** ni DIB.</span><span class="sxs-lookup"><span data-stu-id="a45aa-196">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="a45aa-197">Sin un **HDC,** debe haber otra manera de que la aplicación obtenga los píxeles de mapa de bits para poder copiarlos o usarlos de otro modo.</span><span class="sxs-lookup"><span data-stu-id="a45aa-197">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="a45aa-198">Incluso en Windows, a veces resulta útil obtener los datos de píxeles reales y mostramos la manera actual de hacerlo en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="a45aa-198">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="a45aa-199">Otras diferencias de API entre DWriteCore y DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a45aa-199">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="a45aa-200">Hay algunas API que solo son código auxiliar o se comportan de forma ligeramente diferente en plataformas que no son de Windows.</span><span class="sxs-lookup"><span data-stu-id="a45aa-200">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="a45aa-201">Por ejemplo, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) devuelve **E_NOTIMPL** en plataformas que no son de Windows, ya que no hay nada como **un HDC** sin [GDI.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="a45aa-201">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="a45aa-202">Y, por último, hay otras API de Windows que normalmente se usan junto con DirectWrite (Direct2D es un ejemplo importante).</span><span class="sxs-lookup"><span data-stu-id="a45aa-202">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="a45aa-203">Sin embargo, actualmente, Direct2D y DWriteCore no interoperan.</span><span class="sxs-lookup"><span data-stu-id="a45aa-203">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="a45aa-204">Por ejemplo, si crea un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante DWriteCore y lo pasa a [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), se producirá un error en esa llamada.</span><span class="sxs-lookup"><span data-stu-id="a45aa-204">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
