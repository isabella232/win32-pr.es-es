---
title: Administrador de animaciones de Windows
description: El administrador de animaciones de Windows (animación de Windows) permite una animación enriquecida de elementos de la interfaz de usuario.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animación de Windows animación de Windows, portal
- Animación de Windows del administrador de animaciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995377"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="bb9e0-105">Administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="bb9e0-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="bb9e0-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="bb9e0-106">Purpose</span></span>

<span data-ttu-id="bb9e0-107">El administrador de animaciones de Windows (animación de Windows) permite una animación enriquecida de elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="bb9e0-108">Está diseñado para simplificar el proceso de agregar animación a la interfaz de usuario de una aplicación y permitir a los desarrolladores implementar animaciones que son suaves, naturales e interactivas.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="bb9e0-109">El marco de animaciones administra la programación y la ejecución de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="bb9e0-110">Proporciona una biblioteca de funciones matemáticas útiles para especificar el comportamiento de un elemento de la interfaz de usuario a lo largo del tiempo, y también permite a los desarrolladores implementar funciones personalizadas que proporcionan comportamientos adicionales.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="bb9e0-111">La animación de Windows no realiza la representación; se puede usar con cualquier plataforma de gráficos, como Direct2D, Direct3D o GDI+.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb9e0-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bb9e0-112">In this section</span></span>



| <span data-ttu-id="bb9e0-113">Tema</span><span class="sxs-lookup"><span data-stu-id="bb9e0-113">Topic</span></span>                                                                                   | <span data-ttu-id="bb9e0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9e0-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb9e0-115">Guía de desarrollo de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="bb9e0-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="bb9e0-116">La guía del Desarrollador proporciona información general sobre la animación de Windows y proporciona código de ejemplo que abarca las tareas de animación básicas.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="bb9e0-117">Referencia de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="bb9e0-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="bb9e0-118">Los temas contenidos en esta sección proporcionan las especificaciones de referencia para el administrador de animaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="bb9e0-119">Ejemplos de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="bb9e0-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="bb9e0-120">Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del administrador de animaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="bb9e0-121">Glosario de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="bb9e0-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="bb9e0-122">Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan el administrador de animaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="bb9e0-123">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="bb9e0-123">Developer audience</span></span>

<span data-ttu-id="bb9e0-124">Windows Animation está diseñado para su uso por parte de desarrolladores de C/C++ con experiencia que están familiarizados con COM, los conceptos de programación de la interfaz de usuario y los conceptos de animación generales.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bb9e0-125">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="bb9e0-125">Run-time requirements</span></span>

<span data-ttu-id="bb9e0-126">El administrador de animaciones de Windows se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="bb9e0-127">Las aplicaciones que requieren compatibilidad con el administrador de animaciones de Windows en Windows Vista pueden utilizar la actualización de la plataforma para Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="bb9e0-128">Las aplicaciones que requieren la actualización de la plataforma para Windows Vista pueden tener Windows Update comprobar que está instalada, o bien descargarlas e instalarlas en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="bb9e0-129">Para obtener más información, vea acerca de la [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bb9e0-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb9e0-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bb9e0-130">Additional resources</span></span>

-   <span data-ttu-id="bb9e0-131">[Información general sobre animaciones de Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vídeo)</span><span class="sxs-lookup"><span data-stu-id="bb9e0-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="bb9e0-132">[Dentro de Windows 7: tutorial y análisis en profundidad del administrador de animaciones](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vídeo)</span><span class="sxs-lookup"><span data-stu-id="bb9e0-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="bb9e0-133">[Animación de Windows: temas avanzados](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vídeo)</span><span class="sxs-lookup"><span data-stu-id="bb9e0-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="bb9e0-134">Código de ejemplo del administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="bb9e0-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="bb9e0-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb9e0-135">Related topics</span></span>

[<span data-ttu-id="bb9e0-136">Información general sobre animaciones (.NET Framework)</span><span class="sxs-lookup"><span data-stu-id="bb9e0-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)