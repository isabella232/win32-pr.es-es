---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8223ec5e98db3e45b0087073b4eb68baeae81280
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089183"
---
# <a name="direct2d"></a><span data-ttu-id="4f0c2-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4f0c2-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="4f0c2-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="4f0c2-104">Purpose</span></span>

<span data-ttu-id="4f0c2-105">Direct2D es una API de elementos gráficos 2D con aceleración por hardware y modo inmediato que ofrece alto rendimiento y representación de alta calidad de geometría 2D, mapas de bits y texto.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="4f0c2-106">La API de Direct2D está diseñada para interoperar bien con GDI, GDI+ y Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4f0c2-107">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="4f0c2-107">Developer audience</span></span>

<span data-ttu-id="4f0c2-108">Direct2D está diseñado principalmente para su uso por las siguientes clases de desarrolladores:</span><span class="sxs-lookup"><span data-stu-id="4f0c2-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="4f0c2-109">Desarrolladores de aplicaciones nativas de gran escala empresarial.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="4f0c2-110">Desarrolladores que crean kits de herramientas de control y bibliotecas para su consumo por parte de desarrolladores de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="4f0c2-111">Desarrolladores que requieren la representación del lado servidor de gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="4f0c2-112">Desarrolladores que usan gráficos Direct3D y necesitan una representación 2D y de texto sencilla y de alto rendimiento para menús, elementos de interfaz de usuario (UI) y pantallas de visualización directa (HUD).</span><span class="sxs-lookup"><span data-stu-id="4f0c2-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4f0c2-113">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4f0c2-113">Run-time requirements</span></span>

-   <span data-ttu-id="4f0c2-114">Windows 7 o Windows Vista con Service Pack 2 (SP2) y Actualización de plataforma para Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="4f0c2-115">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y Actualización de plataforma para Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="4f0c2-116">La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 son un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores dirigir aplicaciones a Windows 7, Windows Vista, Windows Server 2008 R2 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="4f0c2-117">Estas actualizaciones estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través Windows Update.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="4f0c2-118">Las aplicaciones de terceros que requieren Actualización de plataforma para Windows Vista o Actualización de plataforma para Windows Server 2008 pueden tener Windows Update detectar si está instalada la actualización necesaria; Si no es así, Windows Update descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="4f0c2-119">Para obtener más información sobre ambas actualizaciones, vea [Actualización de plataforma para Windows Vista.](https://support.microsoft.com/kb/971644)</span><span class="sxs-lookup"><span data-stu-id="4f0c2-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="4f0c2-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4f0c2-120">In this section</span></span>



| <span data-ttu-id="4f0c2-121">Tema</span><span class="sxs-lookup"><span data-stu-id="4f0c2-121">Topic</span></span>                                                                                          | <span data-ttu-id="4f0c2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f0c2-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f0c2-123">Novedades de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4f0c2-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="4f0c2-124">Estas son algunas de las nuevas adiciones a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="4f0c2-125">Acerca de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4f0c2-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="4f0c2-126">Presenta Direct2D, una API que proporciona a los desarrolladores de Win32 la capacidad de realizar tareas de representación de gráficos 2D con un rendimiento y una calidad visual superiores.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="4f0c2-127">Inicio rápido de Direct2D para Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f0c2-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="4f0c2-128">Resume los pasos necesarios para dibujar con Direct2D y proporciona código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="4f0c2-129">Tareas iniciales con Direct2D</span><span class="sxs-lookup"><span data-stu-id="4f0c2-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="4f0c2-130">Describe cómo empezar a crear aplicaciones de Direct2D y proporciona código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="4f0c2-131">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="4f0c2-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="4f0c2-132">Esta sección contiene temas de programación conceptual que describen cómo usar la API de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="4f0c2-133">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4f0c2-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="4f0c2-134">Describe la API de Direct2D en detalle.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="4f0c2-135">Herramientas y utilidades</span><span class="sxs-lookup"><span data-stu-id="4f0c2-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="4f0c2-136">Herramientas y utilidades proporcionadas para Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="4f0c2-137">Muestras</span><span class="sxs-lookup"><span data-stu-id="4f0c2-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="4f0c2-138">Aplicaciones de ejemplo que muestran la API de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="4f0c2-139">Glosario de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4f0c2-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="4f0c2-140">Describe los términos que se usan habitualmente en la documentación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="4f0c2-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4f0c2-141">Additional resources</span></span>

-   [<span data-ttu-id="4f0c2-142">**Gráficos y juegos de DirectX**</span><span class="sxs-lookup"><span data-stu-id="4f0c2-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="4f0c2-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="4f0c2-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

