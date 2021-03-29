---
title: Frontal, posterior y otros búferes
description: OpenGL almacena y manipula datos de píxeles en un fotogramas.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL en Windows, búferes
- framebuffers OpenGL
- búferes de color OpenGL
- búferes de profundidad OpenGL
- búferes de acumulación OpenGL
- búferes de estarcido OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418835"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="c585f-109">Frontal, posterior y otros búferes</span><span class="sxs-lookup"><span data-stu-id="c585f-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="c585f-110">OpenGL almacena y manipula datos de píxeles en un fotogramas.</span><span class="sxs-lookup"><span data-stu-id="c585f-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="c585f-111">Fotogramas consta de un conjunto de búferes lógicos: color, Depth, acumulación y búferes de estarcido.</span><span class="sxs-lookup"><span data-stu-id="c585f-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="c585f-112">El búfer de color se compone de un conjunto de búferes lógicos; Este conjunto puede incluir una parte delantera izquierda, una parte delantera derecha, una parte trasera izquierda, una parte derecha y un número de búferes auxiliares.</span><span class="sxs-lookup"><span data-stu-id="c585f-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="c585f-113">Es posible que un formato de píxel determinado o una implementación de OpenGL no suministren todos estos búferes.</span><span class="sxs-lookup"><span data-stu-id="c585f-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="c585f-114">Por ejemplo, la versión actual de la implementación de OpenGL en Windows de Microsoft no admite imágenes Stereoscopic, por lo que un formato de píxel no puede tener búferes de color a la izquierda y a la derecha.</span><span class="sxs-lookup"><span data-stu-id="c585f-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="c585f-115">Además, la versión actual no admite búferes auxiliares.</span><span class="sxs-lookup"><span data-stu-id="c585f-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="c585f-116">Para obtener más información sobre los búferes OpenGL y las funciones OpenGL que operan en ellos, vea el *manual de referencia de OpenGL* y la guía de programación de *OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="c585f-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="c585f-117">La implementación de OpenGL en Windows de Microsoft admite el doble búfer de imágenes.</span><span class="sxs-lookup"><span data-stu-id="c585f-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="c585f-118">Se trata de una técnica en la que una aplicación dibuja píxeles en un búfer fuera de pantalla y, a continuación, cuando la imagen está lista para mostrarse, copia el contenido del búfer fuera de pantalla en un búfer en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c585f-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="c585f-119">El doble búfer permite cambios de imagen suaves, que son especialmente importantes para las imágenes animadas.</span><span class="sxs-lookup"><span data-stu-id="c585f-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="c585f-120">Dos búferes de color están disponibles para las aplicaciones que utilizan el almacenamiento en búfer doble: un búfer frontal y un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="c585f-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="c585f-121">De forma predeterminada, los comandos de dibujo se dirigen al búfer de reserva (el búfer fuera de pantalla), mientras que el búfer frontal se muestra en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c585f-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="c585f-122">Cuando el búfer fuera de pantalla está listo para su presentación, se llama a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)y Windows copia el contenido del búfer fuera de pantalla en el búfer en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c585f-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="c585f-123">La implementación genérica usa un mapa de bits independiente del dispositivo (DIB) como búfer de reserva y la presentación en pantalla como búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="c585f-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="c585f-124">Los dispositivos de hardware y sus controladores pueden usar enfoques diferentes.</span><span class="sxs-lookup"><span data-stu-id="c585f-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="c585f-125">El almacenamiento en búfer doble es una propiedad de formato de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c585f-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="c585f-126">Para solicitar un doble búfer para un formato de píxel, establezca la \_ marca PFD DOUBLEBUFFER en la estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) en una llamada a [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="c585f-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="c585f-127">La función básica de OpenGL, [**glDrawBuffer**](gldrawbuffer.md), selecciona los búferes para escritura y borrado.</span><span class="sxs-lookup"><span data-stu-id="c585f-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c585f-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c585f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c585f-129">Funciones de búfer</span><span class="sxs-lookup"><span data-stu-id="c585f-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 




