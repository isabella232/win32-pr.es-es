---
title: Por qué usar DirectComposition
description: En este tema se describen las capacidades y ventajas de Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Por qué usar DirectComposition
- razones para usar DirectComposition
- Funcionalidades y ventajas de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695718"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="60f48-106">¿Por qué usar DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="60f48-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="60f48-107">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="60f48-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="60f48-108">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="60f48-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="60f48-109">En este tema se describen las capacidades y ventajas de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="60f48-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="60f48-110">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="60f48-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="60f48-111">Crear una interfaz de usuario visualmente atractiva</span><span class="sxs-lookup"><span data-stu-id="60f48-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="60f48-112">Habilitar animaciones enriquecidas y suaves para la aplicación</span><span class="sxs-lookup"><span data-stu-id="60f48-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="60f48-113">Combinar mapas de bits de diversos orígenes</span><span class="sxs-lookup"><span data-stu-id="60f48-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="60f48-114">Ahorro de memoria mediante la integración con DWM</span><span class="sxs-lookup"><span data-stu-id="60f48-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="60f48-115">Mantenga lo que ya tiene</span><span class="sxs-lookup"><span data-stu-id="60f48-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="60f48-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60f48-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="60f48-117">Crear una interfaz de usuario visualmente atractiva</span><span class="sxs-lookup"><span data-stu-id="60f48-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="60f48-118">DirectComposition permite combinar y animar [*objetos visuales*](directcomposition-glossary.md) para crear una interfaz de usuario visualmente atractiva para las aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="60f48-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="60f48-119">Puede ayudar a dar a la aplicación una apariencia única y establecer una identidad que se aparte de otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="60f48-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="60f48-120">DirectComposition también puede ayudar a facilitar el uso de sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="60f48-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="60f48-121">Por ejemplo, puedes utilizarlo para crear indicaciones visuales y transiciones de pantalla animadas que muestren las relaciones entre los elementos de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="60f48-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="60f48-122">Habilitar animaciones enriquecidas y suaves para la aplicación</span><span class="sxs-lookup"><span data-stu-id="60f48-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="60f48-123">DirectComposition es un motor de composición de mapas de bits de alto rendimiento que usa gráficos acelerados por hardware para lograr velocidades de fotogramas altas, lo que produce una panorámica, un desplazamiento y animaciones de contenido complejo suaves y coherentes.</span><span class="sxs-lookup"><span data-stu-id="60f48-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="60f48-124">Dado que funciona en un subproceso dedicado que es independiente del subproceso utilizado para representar la interfaz de usuario de la aplicación, DirectComposition nunca puede "privar" el subproceso de la interfaz de usuario ni interferir con la capacidad de la aplicación para dibujar sus elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="60f48-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="60f48-125">Combinar mapas de bits de diversos orígenes</span><span class="sxs-lookup"><span data-stu-id="60f48-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="60f48-126">Muchas aplicaciones basadas en Windows tienen una interfaz de usuario formada por elementos creados por una variedad de marcos de gráficos diferentes.</span><span class="sxs-lookup"><span data-stu-id="60f48-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="60f48-127">Por ejemplo, una aplicación podría usar Windows Forms para crear una barra de estado, Windows Interfaz de dispositivo gráfico (GDI) para crear el contenido de la ventana principal, el contenido de Microsoft DirectX para gráficos, etc.</span><span class="sxs-lookup"><span data-stu-id="60f48-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="60f48-128">DirectComposition permite combinar el contenido de una variedad de marcos de gráficos y hacer que se represente en la misma ventana secundaria o de nivel superior sin necesidad de preocuparse de lo que sucede si se superpone el contenido de marcos de trabajo diferentes.</span><span class="sxs-lookup"><span data-stu-id="60f48-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="60f48-129">Ahorro de memoria mediante la integración con DWM</span><span class="sxs-lookup"><span data-stu-id="60f48-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="60f48-130">Las composiciones y animaciones creadas por DirectComposition se pasan a un componente integrado de Windows llamado [Administrador de ventanas de escritorio (DWM)](/windows/desktop/dwm/dwm-overview) para la representación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="60f48-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="60f48-131">Por lo tanto, no se requieren componentes de representación especiales ni marcos de interfaz de usuario en el equipo.</span><span class="sxs-lookup"><span data-stu-id="60f48-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="60f48-132">Mantenga lo que ya tiene</span><span class="sxs-lookup"><span data-stu-id="60f48-132">Keep what you already have</span></span>

<span data-ttu-id="60f48-133">El código de la interfaz de usuario de una aplicación existente basada en Windows representa una inversión significativa.</span><span class="sxs-lookup"><span data-stu-id="60f48-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="60f48-134">En su mayor parte, DirectComposition le permite crear y animar el contenido de la interfaz de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="60f48-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="60f48-135">Esto significa que puede usar DirectComposition para realizar actualizaciones y mejoras importantes en la interfaz de usuario de la aplicación sin necesidad de realizar cambios significativos en la base de código de interfaz de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="60f48-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60f48-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60f48-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60f48-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="60f48-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 