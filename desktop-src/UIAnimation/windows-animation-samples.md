---
title: Ejemplos de animación de Windows
description: Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del administrador de animaciones de Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animación de Windows animación de Windows, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357514"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="8cf10-104">Ejemplos de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="8cf10-104">Windows Animation Samples</span></span>

<span data-ttu-id="8cf10-105">Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del administrador de animaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="8cf10-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8cf10-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8cf10-106">In this section</span></span>



| <span data-ttu-id="8cf10-107">Tema</span><span class="sxs-lookup"><span data-stu-id="8cf10-107">Topic</span></span>                                                                                     | <span data-ttu-id="8cf10-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cf10-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cf10-109">Ejemplo de animación controlada por la aplicación</span><span class="sxs-lookup"><span data-stu-id="8cf10-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="8cf10-110">Ejemplo de animación controlada por temporizador</span><span class="sxs-lookup"><span data-stu-id="8cf10-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="8cf10-111">Ejemplo de interpolador personalizado</span><span class="sxs-lookup"><span data-stu-id="8cf10-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="8cf10-112">Muestra cómo usar la animación de Windows con su propio interpolador personalizado, con Direct2D usado para la representación.</span><span class="sxs-lookup"><span data-stu-id="8cf10-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="8cf10-113">Ejemplo de diseño de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="8cf10-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="8cf10-114">Muestra cómo usar la animación de Windows, utilizando Direct2D para animar una cuadrícula de imágenes.</span><span class="sxs-lookup"><span data-stu-id="8cf10-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="8cf10-115">Ejemplo de comparación de prioridades</span><span class="sxs-lookup"><span data-stu-id="8cf10-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="8cf10-116">Muestra cómo usar la animación de Windows con su propia comparación de prioridad mediante Direct2D para la representación.</span><span class="sxs-lookup"><span data-stu-id="8cf10-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="8cf10-117">Archivos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8cf10-117">Sample Files</span></span>

<span data-ttu-id="8cf10-118">Cada ejemplo contiene muchos de los siguientes archivos de clave:</span><span class="sxs-lookup"><span data-stu-id="8cf10-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="8cf10-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp</span><span class="sxs-lookup"><span data-stu-id="8cf10-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-120">Define el punto de entrada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cf10-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="8cf10-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h</span><span class="sxs-lookup"><span data-stu-id="8cf10-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-122">Declara la clase CMainWindow.</span><span class="sxs-lookup"><span data-stu-id="8cf10-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="8cf10-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp</span><span class="sxs-lookup"><span data-stu-id="8cf10-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-124">Inicializa los componentes de animación y la plataforma de gráficos, carga imágenes y representa el área cliente.</span><span class="sxs-lookup"><span data-stu-id="8cf10-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="8cf10-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h</span><span class="sxs-lookup"><span data-stu-id="8cf10-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-126">Declara la clase CLayoutManager.</span><span class="sxs-lookup"><span data-stu-id="8cf10-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="8cf10-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp</span><span class="sxs-lookup"><span data-stu-id="8cf10-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-128">Calcula el diseño de las imágenes en la ventana principal, crea guiones gráficos, agrega transiciones al guion gráfico y programa el guión gráfico.</span><span class="sxs-lookup"><span data-stu-id="8cf10-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="8cf10-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail. h</span><span class="sxs-lookup"><span data-stu-id="8cf10-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-130">Declara la clase CThumbNail.</span><span class="sxs-lookup"><span data-stu-id="8cf10-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="8cf10-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail. cpp</span><span class="sxs-lookup"><span data-stu-id="8cf10-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="8cf10-132">Crea variables de animación y representa vistas en miniatura.</span><span class="sxs-lookup"><span data-stu-id="8cf10-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8cf10-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cf10-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf10-134">Guía de desarrollo de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="8cf10-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="8cf10-135">Referencia de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="8cf10-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 





