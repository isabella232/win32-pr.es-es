---
title: Introducción a la API de ampliación
description: En este tema se describe la API de ampliación y se explica cómo utilizarla en una aplicación.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Aumento
- aplicaciones de ampliación de pantalla
- Aumento
- procesamiento de imágenes personalizadas
- Magnification.dll
- crear controles del ampliador
- Ampliación selectiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720156"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="a6002-110">Introducción a la API de ampliación</span><span class="sxs-lookup"><span data-stu-id="a6002-110">Magnification API Overview</span></span>

<span data-ttu-id="a6002-111">La API de ampliación permite a los proveedores de tecnología de asistencia desarrollar aplicaciones de ampliación de pantalla que se ejecutan en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a6002-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="a6002-112">En este tema se describe la API de ampliación y se explica cómo utilizarla en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6002-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="a6002-113">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6002-113">It contains the following sections:</span></span>

- [<span data-ttu-id="a6002-114">Introducción</span><span class="sxs-lookup"><span data-stu-id="a6002-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="a6002-115">Conceptos básicos</span><span class="sxs-lookup"><span data-stu-id="a6002-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="a6002-116">Tipos de ampliadores</span><span class="sxs-lookup"><span data-stu-id="a6002-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="a6002-117">Factor de ampliación</span><span class="sxs-lookup"><span data-stu-id="a6002-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="a6002-118">Efectos de color</span><span class="sxs-lookup"><span data-stu-id="a6002-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="a6002-119">Rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="a6002-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="a6002-120">Lista de filtros</span><span class="sxs-lookup"><span data-stu-id="a6002-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="a6002-121">Transformación de entrada</span><span class="sxs-lookup"><span data-stu-id="a6002-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="a6002-122">Cursor del sistema</span><span class="sxs-lookup"><span data-stu-id="a6002-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="a6002-123">Inicializar la biblioteca en tiempo de ejecución del ampliador</span><span class="sxs-lookup"><span data-stu-id="a6002-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="a6002-124">Uso del ampliador de Full-Screen</span><span class="sxs-lookup"><span data-stu-id="a6002-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="a6002-125">Usar el control Magnifier</span><span class="sxs-lookup"><span data-stu-id="a6002-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="a6002-126">Crear el control ampliador</span><span class="sxs-lookup"><span data-stu-id="a6002-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="a6002-127">Inicializar el control</span><span class="sxs-lookup"><span data-stu-id="a6002-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="a6002-128">Establecer el rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="a6002-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="a6002-129">Aplicar efectos de color</span><span class="sxs-lookup"><span data-stu-id="a6002-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="a6002-130">Ampliación selectiva</span><span class="sxs-lookup"><span data-stu-id="a6002-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="a6002-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6002-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="a6002-132">Introducción</span><span class="sxs-lookup"><span data-stu-id="a6002-132">Getting Started</span></span>

<span data-ttu-id="a6002-133">La versión original de la API de ampliación es compatible con Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6002-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="a6002-134">En Windows 8 y versiones posteriores, la API admite características adicionales, incluida la ampliación a pantalla completa y el establecimiento de la visibilidad del cursor del sistema ampliado.</span><span class="sxs-lookup"><span data-stu-id="a6002-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="a6002-135">Magnification.dll proporciona compatibilidad con la API de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="a6002-136">Para compilar la aplicación, incluya proprof. h y vincule a Amplification. lib.</span><span class="sxs-lookup"><span data-stu-id="a6002-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="a6002-137">La API de ampliación no se admite en WOW64; es decir, una aplicación del ampliador de 32 bits no se ejecutará correctamente en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a6002-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="a6002-138">Conceptos básicos</span><span class="sxs-lookup"><span data-stu-id="a6002-138">Basic Concepts</span></span>

<span data-ttu-id="a6002-139">En esta sección se describen los conceptos fundamentales en los que se basa la API de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="a6002-140">Contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="a6002-140">It contains the following parts:</span></span>

- [<span data-ttu-id="a6002-141">Tipos de ampliadores</span><span class="sxs-lookup"><span data-stu-id="a6002-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="a6002-142">Factor de ampliación</span><span class="sxs-lookup"><span data-stu-id="a6002-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="a6002-143">Efectos de color</span><span class="sxs-lookup"><span data-stu-id="a6002-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="a6002-144">Rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="a6002-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="a6002-145">Lista de filtros</span><span class="sxs-lookup"><span data-stu-id="a6002-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="a6002-146">Transformación de entrada</span><span class="sxs-lookup"><span data-stu-id="a6002-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="a6002-147">Cursor del sistema</span><span class="sxs-lookup"><span data-stu-id="a6002-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="a6002-148">Tipos de ampliadores</span><span class="sxs-lookup"><span data-stu-id="a6002-148">Types of Magnifiers</span></span>

<span data-ttu-id="a6002-149">La API admite dos tipos de ampliadores, el *ampliador de pantalla completa* y el *control ampliador*.</span><span class="sxs-lookup"><span data-stu-id="a6002-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="a6002-150">El ampliador de pantalla completa amplía el contenido de toda la pantalla, mientras que el control ampliador amplía el contenido de un área determinada de la pantalla y muestra el contenido en una ventana.</span><span class="sxs-lookup"><span data-stu-id="a6002-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="a6002-151">En el caso de los ampliadores, las imágenes y el texto se amplían y ambos le permiten controlar la cantidad de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="a6002-152">También puede aplicar efectos de color al contenido de la pantalla ampliada, lo que facilita la visualización de las personas que tienen deficiencias de color o necesitan colores con mayor o menor contraste.</span><span class="sxs-lookup"><span data-stu-id="a6002-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="a6002-153">La API del control Magnifier está disponible en Windows Vista y sistemas operativos posteriores, mientras que la API del ampliador de pantalla completa solo está disponible en los sistemas operativos Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6002-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="a6002-154">Factor de ampliación</span><span class="sxs-lookup"><span data-stu-id="a6002-154">Magnification Factor</span></span>

<span data-ttu-id="a6002-155">Tanto el ampliador de pantalla completa como el control ampliador aplican una transformación de escala al contenido de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="a6002-156">La cantidad de ampliación aplicada por la transformación de escala se denomina *factor de ampliación*.</span><span class="sxs-lookup"><span data-stu-id="a6002-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="a6002-157">Se expresa como un valor de punto flotante, en el que 1,0 corresponde a ninguna ampliación y los valores más grandes dan como resultado una cantidad de ampliación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a6002-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="a6002-158">Por ejemplo, un valor de 1,5 hace que el contenido de la pantalla sea 50 por ciento más grande.</span><span class="sxs-lookup"><span data-stu-id="a6002-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="a6002-159">Un factor de ampliación inferior a 1,0 no es válido.</span><span class="sxs-lookup"><span data-stu-id="a6002-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="a6002-160">Efectos de color</span><span class="sxs-lookup"><span data-stu-id="a6002-160">Color Effects</span></span>

<span data-ttu-id="a6002-161">Los efectos de color se logran aplicando una matriz de transformación de color 5 por 5 a los colores del contenido de la pantalla ampliada.</span><span class="sxs-lookup"><span data-stu-id="a6002-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="a6002-162">La matriz determina las intensidades de los componentes rojo, azul, verde y alfa del contenido.</span><span class="sxs-lookup"><span data-stu-id="a6002-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="a6002-163">Para obtener más información, vea [usar una matriz de colores para transformar un solo color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) en la documentación de Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="a6002-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="a6002-164">Rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="a6002-164">Source Rectangle</span></span>

<span data-ttu-id="a6002-165">El ampliador de pantalla completa aplica la transformación de escala y la transformación de color a toda la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="a6002-166">Por otro lado, el control ampliador copia un área de la pantalla, denominada *rectángulo de origen*, en un mapa de bits fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="a6002-167">Después, el control aplica la transformación de escala y la transformación de color, si existe, al mapa de bits fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="a6002-168">Por último, el control muestra el mapa de bits escalado y transformado por colores en la ventana de control del ampliador.</span><span class="sxs-lookup"><span data-stu-id="a6002-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="a6002-169">Lista de filtros</span><span class="sxs-lookup"><span data-stu-id="a6002-169">Filter List</span></span>

<span data-ttu-id="a6002-170">De forma predeterminada, el control Magnifier amplía todas las ventanas del rectángulo de origen especificado.</span><span class="sxs-lookup"><span data-stu-id="a6002-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="a6002-171">Sin embargo, al proporcionar una *lista de filtros* de identificadores de ventana, puede controlar qué ventanas se incluyen en el contenido ampliado y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="a6002-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="a6002-172">Para obtener más información, vea el apartado sobre el [aumento selectivo](#selective-magnification).</span><span class="sxs-lookup"><span data-stu-id="a6002-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="a6002-173">El ampliador de pantalla completa no es compatible con una lista de filtros; siempre amplía todas las ventanas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="a6002-174">Transformación de entrada</span><span class="sxs-lookup"><span data-stu-id="a6002-174">Input Transform</span></span>

<span data-ttu-id="a6002-175">Normalmente, el contenido de la pantalla ampliada es "invisible" para el lápiz de usuario o la entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="a6002-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="a6002-176">Por ejemplo, si el usuario pulsa la imagen ampliada de un control, el sistema no pasa necesariamente la entrada al control.</span><span class="sxs-lookup"><span data-stu-id="a6002-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="a6002-177">En su lugar, el sistema pasa la entrada a cualquier elemento (si existe) que se encuentra en las coordenadas de la pantalla punteada en el escritorio sin ampliar.</span><span class="sxs-lookup"><span data-stu-id="a6002-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="a6002-178">La función [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) permite especificar una transformación de *entrada* que asigna el espacio de coordenadas del contenido de la pantalla ampliada al espacio de coordenadas de pantalla real (no ampliado).</span><span class="sxs-lookup"><span data-stu-id="a6002-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="a6002-179">Esto permite al sistema pasar la entrada táctil o manuscrita que se escribe en el contenido de la pantalla ampliada, al elemento de la interfaz de usuario correcto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="a6002-180">El proceso de llamada debe tener privilegios UIAccess para establecer la transformación de entrada.</span><span class="sxs-lookup"><span data-stu-id="a6002-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="a6002-181">Para obtener más información, vea [consideraciones de seguridad de UI Automation](../uiauto-securityoverview.md) y [/manifestuac (insertar información de UAC en el manifiesto)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span><span class="sxs-lookup"><span data-stu-id="a6002-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="a6002-182">Cursor del sistema</span><span class="sxs-lookup"><span data-stu-id="a6002-182">System Cursor</span></span>

<span data-ttu-id="a6002-183">La función [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) permite mostrar u ocultar el cursor del sistema.</span><span class="sxs-lookup"><span data-stu-id="a6002-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="a6002-184">Si se muestra el cursor del sistema cuando el ampliador de pantalla completa está activo, el cursor del sistema siempre se amplía junto con el resto del contenido de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="a6002-185">Si oculta el cursor del sistema cuando el ampliador de pantalla completa está activo, el cursor del sistema no es visible en absoluto.</span><span class="sxs-lookup"><span data-stu-id="a6002-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="a6002-186">Con el control Magnifier, la función [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) muestra u oculta el cursor del sistema no ampliado, pero no tiene ningún efecto en el cursor del sistema ampliado.</span><span class="sxs-lookup"><span data-stu-id="a6002-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="a6002-187">La visibilidad del cursor del sistema ampliado depende de si el control de la lupa tiene el estilo [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a6002-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="a6002-188">Si tiene este estilo, el control ampliador muestra el cursor del sistema ampliado, junto con el contenido de la pantalla ampliada, siempre que el cursor del sistema entre en el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="a6002-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="a6002-189">Inicializar la biblioteca en tiempo de ejecución del ampliador</span><span class="sxs-lookup"><span data-stu-id="a6002-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="a6002-190">Antes de poder llamar a cualquier otra función de API del ampliador, debe crear e inicializar los objetos de tiempo de ejecución del ampliador mediante una llamada a la función [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) .</span><span class="sxs-lookup"><span data-stu-id="a6002-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="a6002-191">Del mismo modo, después de terminar de usar la API del ampliador, llame a la función [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) para destruir los objetos de tiempo de ejecución del ampliador y liberar los recursos del sistema asociados.</span><span class="sxs-lookup"><span data-stu-id="a6002-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="a6002-192">Uso del ampliador de Full-Screen</span><span class="sxs-lookup"><span data-stu-id="a6002-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="a6002-193">Para usar el ampliador de pantalla completa, llame a la función [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="a6002-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="a6002-194">El parámetro *magLevel* especifica el factor de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="a6002-195">Los parámetros *xoffset* y *YOFFSET* especifican cómo se coloca el contenido de la pantalla ampliada en relación con la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="a6002-196">Cuando se amplía el contenido de la pantalla, se vuelve más grande que la propia pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="a6002-197">Parte del contenido se extiende más allá de los bordes de la pantalla y se convierte en invisible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a6002-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="a6002-198">Los parámetros *xoffset* y *YOFFSET* de la función [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) determinan qué parte del contenido de la pantalla ampliada aparece en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="a6002-199">Juntos, los parámetros especifican las coordenadas de un punto en el contenido de pantalla no ampliada.</span><span class="sxs-lookup"><span data-stu-id="a6002-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="a6002-200">Cuando se amplía el contenido, se coloca con el punto especificado en la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="a6002-201">En el ejemplo siguiente se establece el factor de ampliación para el ampliador de pantalla completa y se coloca el centro del contenido de la pantalla ampliada en el centro de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="a6002-202">Utilice la función [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) para aplicar efectos de color al contenido de pantalla completa mediante el establecimiento de una matriz de transformación de color definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6002-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="a6002-203">Por ejemplo, en el ejemplo siguiente se establece una matriz de transformación de color que convierte los colores a escala de grises.</span><span class="sxs-lookup"><span data-stu-id="a6002-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="a6002-204">Puede recuperar el factor de ampliación actual y los valores de desplazamiento mediante una llamada a la función [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="a6002-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="a6002-205">Puede recuperar la matriz de transformación de color actual llamando a la función [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .</span><span class="sxs-lookup"><span data-stu-id="a6002-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="a6002-206">Usar el control Magnifier</span><span class="sxs-lookup"><span data-stu-id="a6002-206">Using the Magnifier Control</span></span>

<span data-ttu-id="a6002-207">El control ampliador amplía el contenido de un área determinada de la pantalla y muestra el contenido en una ventana.</span><span class="sxs-lookup"><span data-stu-id="a6002-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="a6002-208">En esta sección se describe cómo usar el control ampliador.</span><span class="sxs-lookup"><span data-stu-id="a6002-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="a6002-209">Contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="a6002-209">It contains the following parts:</span></span>

- [<span data-ttu-id="a6002-210">Crear el control ampliador</span><span class="sxs-lookup"><span data-stu-id="a6002-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="a6002-211">Inicializar el control</span><span class="sxs-lookup"><span data-stu-id="a6002-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="a6002-212">Establecer el rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="a6002-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="a6002-213">Aplicar efectos de color</span><span class="sxs-lookup"><span data-stu-id="a6002-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="a6002-214">Ampliación selectiva</span><span class="sxs-lookup"><span data-stu-id="a6002-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="a6002-215">Crear el control ampliador</span><span class="sxs-lookup"><span data-stu-id="a6002-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="a6002-216">El control ampliador debe estar hospedado en una ventana creada con el estilo extendido [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a6002-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="a6002-217">Después de crear la ventana host, llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) para establecer la opacidad de la ventana host.</span><span class="sxs-lookup"><span data-stu-id="a6002-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="a6002-218">La ventana host normalmente se establece en opacidad completa para evitar que se muestre el contenido de la pantalla subyacente.</span><span class="sxs-lookup"><span data-stu-id="a6002-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="a6002-219">En el ejemplo siguiente se muestra cómo establecer la ventana host en la opacidad completa:</span><span class="sxs-lookup"><span data-stu-id="a6002-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="a6002-220">Si aplica el estilo [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) a la ventana host, los clics del mouse se pasan a cualquier objeto situado detrás de la ventana host en la ubicación del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="a6002-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="a6002-221">Tenga en cuenta que, dado que la ventana host no procesa los clics del mouse, el usuario no podrá moverse ni cambiar el tamaño de la ventana de ampliación mediante el mouse.</span><span class="sxs-lookup"><span data-stu-id="a6002-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="a6002-222">La clase de ventana de la ventana de control del ampliador debe estar **WC_MAGNIFIER**.</span><span class="sxs-lookup"><span data-stu-id="a6002-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="a6002-223">Si aplica el estilo [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , el control ampliador incluye el cursor del sistema en el contenido de la pantalla ampliada y el cursor se amplía junto con el contenido de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6002-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="a6002-224">Después de crear el control ampliador, mantenga el identificador de ventana para que pueda pasarlo a otras funciones.</span><span class="sxs-lookup"><span data-stu-id="a6002-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="a6002-225">En el ejemplo siguiente se muestra cómo crear el control ampliador.</span><span class="sxs-lookup"><span data-stu-id="a6002-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="a6002-226">Inicializar el control</span><span class="sxs-lookup"><span data-stu-id="a6002-226">Initializing the Control</span></span>

<span data-ttu-id="a6002-227">Después de crear el control Magnifier, debe llamar a la función [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) para especificar el factor de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="a6002-228">Esto es simplemente una cuestión de especificar una matriz de</span><span class="sxs-lookup"><span data-stu-id="a6002-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="a6002-229">(*n*, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="a6002-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="a6002-230">(0,0, *n*, 0,0)</span><span class="sxs-lookup"><span data-stu-id="a6002-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="a6002-231">(0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="a6002-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="a6002-232">donde *n* es el factor de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="a6002-233">En el ejemplo siguiente se muestra cómo establecer el factor de ampliación para el control ampliador.</span><span class="sxs-lookup"><span data-stu-id="a6002-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="a6002-234">Establecer el rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="a6002-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="a6002-235">A medida que el usuario mueve el cursor del mouse alrededor de la pantalla, la aplicación llama a la función [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) para especificar la parte de la pantalla subyacente que se va a ampliar.</span><span class="sxs-lookup"><span data-stu-id="a6002-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="a6002-236">La función de ejemplo siguiente calcula la posición y las dimensiones del rectángulo de origen (en función de la posición del mouse y las dimensiones de la ventana del ampliador dividido por el factor de ampliación) y establece el rectángulo de origen en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="a6002-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="a6002-237">La función también centra el área cliente de la ventana host en la posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="a6002-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="a6002-238">Esta función se llamaría a intervalos para actualizar la ventana de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="a6002-239">Aplicar efectos de color</span><span class="sxs-lookup"><span data-stu-id="a6002-239">Applying Color Effects</span></span>

<span data-ttu-id="a6002-240">Un control ampliador que tiene el estilo [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) aplica una matriz de transformación de color integrada que invierte los colores del contenido de la pantalla ampliada.</span><span class="sxs-lookup"><span data-stu-id="a6002-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="a6002-241">En la ilustración siguiente se muestra el contenido de la pantalla en un control ampliador que tiene el estilo **MS_INVERTCOLORS** .</span><span class="sxs-lookup"><span data-stu-id="a6002-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![captura de pantalla del contenido ampliado con colores invertidos](images/color-inversion.png)

<span data-ttu-id="a6002-243">La función [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) permite aplicar otros efectos de color estableciendo una matriz de transformación de color definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6002-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="a6002-244">Por ejemplo, la función siguiente establece una matriz de transformación de color que convierte los colores a escala de grises.</span><span class="sxs-lookup"><span data-stu-id="a6002-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="a6002-245">Para obtener más información sobre cómo funcionan las transformaciones de color, vea [usar una matriz de colores para transformar un color único](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) en la documentación de GDI+.</span><span class="sxs-lookup"><span data-stu-id="a6002-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="a6002-246">Ampliación selectiva</span><span class="sxs-lookup"><span data-stu-id="a6002-246">Selective Magnification</span></span>

<span data-ttu-id="a6002-247">De forma predeterminada, la ampliación se aplica a todas las ventanas que no sean la propia ventana de ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="a6002-248">Para especificar qué ventanas se van a ampliar, llame a la función [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) .</span><span class="sxs-lookup"><span data-stu-id="a6002-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="a6002-249">Este método toma una lista de ventanas para aumentar o una lista de ventanas que se van a excluir de la ampliación.</span><span class="sxs-lookup"><span data-stu-id="a6002-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6002-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6002-250">Related topics</span></span>

[<span data-ttu-id="a6002-251">API de ampliación</span><span class="sxs-lookup"><span data-stu-id="a6002-251">Magnification API</span></span>](entry-magapi-sdk.md)