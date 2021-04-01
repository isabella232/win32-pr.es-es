---
title: Direct2D y High-PPP
description: Describe la forma en que Direct2D acomoda la visualización de PPP alta.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, alta PPP
- alta PPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995574"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="1df32-105">Direct2D y High-PPP</span><span class="sxs-lookup"><span data-stu-id="1df32-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="1df32-106">Escribir una aplicación compatible con PPP es la clave para que una interfaz de usuario (UI) tenga un aspecto coherente en una amplia variedad de valores de pantalla de alta ppp.</span><span class="sxs-lookup"><span data-stu-id="1df32-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="1df32-107">Una aplicación que no sea compatible con PPP pero que se esté ejecutando en una configuración de pantalla de valores altos de PPP puede verse afectada por muchos artefactos visuales, incluidos el escalado incorrecto de los elementos de la interfaz de usuario, el texto recortado y las imágenes borrosas.</span><span class="sxs-lookup"><span data-stu-id="1df32-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="1df32-108">Al agregar compatibilidad en la aplicación para el reconocimiento de PPP, se hace que la presentación de la interfaz de usuario de la aplicación sea más predecible, lo que hace que sea más atractiva y fácil de leer para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1df32-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="1df32-109">Afortunadamente, Direct2D facilita más que nunca la escritura de aplicaciones que funcionan bien en un valor alto de PPP.</span><span class="sxs-lookup"><span data-stu-id="1df32-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="1df32-110">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="1df32-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1df32-111">Compatibilidad con alto nivel de PPP en Direct2D</span><span class="sxs-lookup"><span data-stu-id="1df32-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="1df32-112">Windows 8 y alta PPP</span><span class="sxs-lookup"><span data-stu-id="1df32-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="1df32-113">¿Qué es una DIP?</span><span class="sxs-lookup"><span data-stu-id="1df32-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="1df32-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1df32-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="1df32-115">Compatibilidad con alto nivel de PPP en Direct2D</span><span class="sxs-lookup"><span data-stu-id="1df32-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="1df32-116">Direct2D proporciona las siguientes características para trabajar con escenarios de alta PPP:</span><span class="sxs-lookup"><span data-stu-id="1df32-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="1df32-117">Respeta automáticamente el valor de PPP del sistema al crear un destino de representación en ventanas, siempre y cuando el manifiesto de aplicación indique que la aplicación controla el valor de PPP correctamente.</span><span class="sxs-lookup"><span data-stu-id="1df32-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="1df32-118">(Para obtener información sobre cómo declarar que la aplicación tiene reconocimiento de PPP, consulte [Cómo asegurarse de que la aplicación se muestra correctamente en pantallas de alta PPP](how-to--size-a-window-properly-for-high-dpi-displays.md)).</span><span class="sxs-lookup"><span data-stu-id="1df32-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="1df32-119">Expresa las coordenadas en DIP (píxeles independientes del dispositivo), lo que permite que la aplicación se escale automáticamente cuando cambie la configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="1df32-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="1df32-120">Permite que los mapas de bits tengan un PPP y los escala correctamente tomando en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="1df32-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="1df32-121">Esta característica también se puede usar para mantener iconos en diferentes resoluciones.</span><span class="sxs-lookup"><span data-stu-id="1df32-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="1df32-122">Expresa la mayoría de los recursos en DIP, lo que hace que los recursos sean independientes de la resolución.</span><span class="sxs-lookup"><span data-stu-id="1df32-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="1df32-123">Utiliza un espacio de coordenadas de punto flotante y un suavizado de contorno, por lo que cualquier contenido se puede escalar a cualquier PPP arbitrario.</span><span class="sxs-lookup"><span data-stu-id="1df32-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="1df32-124">La canalización de gráficos de Direct2D está diseñada para escalar de 96 PPP a 1200DPI.</span><span class="sxs-lookup"><span data-stu-id="1df32-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="1df32-125">Windows 8 y alta PPP</span><span class="sxs-lookup"><span data-stu-id="1df32-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="1df32-126">A partir de Windows 8, hay características adicionales para la compatibilidad con alta calidad de PPP.</span><span class="sxs-lookup"><span data-stu-id="1df32-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="1df32-127">Si el PPP del contexto del dispositivo es suficientemente alto, Direct2D cambia el umbral que usa para habilitar el suavizado de contorno vertical del texto.</span><span class="sxs-lookup"><span data-stu-id="1df32-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="1df32-128">Esto da como resultado una representación de texto más rápida en pantallas de alta ppp.</span><span class="sxs-lookup"><span data-stu-id="1df32-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="1df32-129">Además, puede cambiar el modo de unidad a píxeles en lugar de a DIP mediante el método [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="1df32-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="1df32-130">Si establece el modo de unidad en píxeles y el valor de PPP del contexto del dispositivo en el valor de PPP de la pantalla, la optimización sigue estando habilitada.</span><span class="sxs-lookup"><span data-stu-id="1df32-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="1df32-131">¿Qué es una DIP?</span><span class="sxs-lookup"><span data-stu-id="1df32-131">What is a DIP?</span></span>

<span data-ttu-id="1df32-132">Un píxel independiente del dispositivo (DIP) es un píxel lógico que se asigna a los píxeles del dispositivo físico a través de un escalar, el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="1df32-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="1df32-133">PPP significa puntos por pulgada, donde un punto representa un píxel de dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="1df32-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="1df32-134">(La nomenclatura procede de la impresión, donde los puntos son el punto de tinta más pequeño que puede producir un proceso de impresión).</span><span class="sxs-lookup"><span data-stu-id="1df32-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="1df32-135">Dado que un monitor estándar solía tener 96 puntos por pulgada, un DPI de 96 significaba que un píxel independiente del dispositivo (o DIP) asigna 1:1 con un píxel físico.</span><span class="sxs-lookup"><span data-stu-id="1df32-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="1df32-136">Por ejemplo, si los PPP fueran 96 \* 2 = 192, una sola DIP abarcaría dos píxeles físicos.</span><span class="sxs-lookup"><span data-stu-id="1df32-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="1df32-137">Hay muchas razones por las que las aplicaciones no controlan necesariamente este ajuste de escala correctamente; uno de los motivos más sencillos es que requiere un trabajo adicional para detectar y usar este valor escalar cuando se representa.</span><span class="sxs-lookup"><span data-stu-id="1df32-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="1df32-138">En Direct2D, el escalado se aplica de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1df32-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="1df32-139">Debido a esta asignación, los píxeles del dispositivo físico pueden acabar en coordenadas DIP fraccionarias, que es uno de los motivos por los que Direct2D usa un espacio de coordenadas de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="1df32-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="1df32-140">píxel físico = (DIP × PPP)/96</span><span class="sxs-lookup"><span data-stu-id="1df32-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="1df32-141">Para convertir un píxel físico en una DIP, use esta fórmula:</span><span class="sxs-lookup"><span data-stu-id="1df32-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="1df32-142">DIP = (píxel físico × 96)/PPP</span><span class="sxs-lookup"><span data-stu-id="1df32-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="1df32-143">A partir de Windows 8, puede cambiar el modo de unidad a píxeles en lugar de a DIP mediante el método [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="1df32-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1df32-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1df32-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df32-145">Cómo asegurarse de que la aplicación se muestre correctamente en pantallas de alta resolución de PPP</span><span class="sxs-lookup"><span data-stu-id="1df32-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 