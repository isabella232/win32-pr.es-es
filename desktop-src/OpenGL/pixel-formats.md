---
title: Formatos de píxeles
description: Formatos de píxeles
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL en Windows, píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665737"
---
# <a name="pixel-formats"></a><span data-ttu-id="8f9c9-104">Formatos de píxeles</span><span class="sxs-lookup"><span data-stu-id="8f9c9-104">Pixel Formats</span></span>

<span data-ttu-id="8f9c9-105">Un *formato de píxel* especifica varias propiedades de una superficie de dibujo de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="8f9c9-106">Algunas de las propiedades especificadas por un formato de píxel son:</span><span class="sxs-lookup"><span data-stu-id="8f9c9-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="8f9c9-107">Si el búfer de píxeles es de un solo valor o de doble búfer.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="8f9c9-108">Indica si los datos de píxeles están en formato RGBA o de índice de color.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="8f9c9-109">Número de bits utilizados para almacenar los datos de color.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="8f9c9-110">Número de bits utilizados para el búfer de profundidad (eje z).</span><span class="sxs-lookup"><span data-stu-id="8f9c9-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="8f9c9-111">Número de bits utilizados para el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="8f9c9-112">El número de planos superpuesto y proporcionaban.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="8f9c9-113">Varias máscaras de visibilidad.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-113">Various visibility masks.</span></span>

<span data-ttu-id="8f9c9-114">La implementación de OpenGL para Windows de Microsoft usa la estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) para transmitir los datos con formato de píxeles.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="8f9c9-115">Los miembros de la estructura especifican las propiedades anteriores y otras.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="8f9c9-116">Un contexto de dispositivo determinado puede admitir varios formatos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="8f9c9-117">Windows identifica los formatos de píxel que admite un contexto de dispositivo con valores de índice de base uno consecutivos (1, 2, 3, 4, etc.).</span><span class="sxs-lookup"><span data-stu-id="8f9c9-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="8f9c9-118">Un contexto de dispositivo solo puede tener un formato de píxel actual, elegido en el conjunto de formatos de píxel que admite.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="8f9c9-119">Cada ventana tiene su propio formato de píxel actual en OpenGL en Windows.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="8f9c9-120">Esto significa, por ejemplo, que una aplicación puede mostrar simultáneamente las ventanas de OpenGL de índice de color y RGBA, o bien las ventanas OpenGL de un solo y doble búfer.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="8f9c9-121">Esta capacidad de formato de píxel por ventana está limitada a las ventanas de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="8f9c9-122">Normalmente, se obtiene un contexto de dispositivo, se establece el formato de píxel del contexto del dispositivo y, a continuación, se crea un contexto de representación de OpenGL adecuado para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="8f9c9-123">Establezca el formato de píxel antes de crear un contexto de representación porque el contexto de representación hereda el formato de píxel del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f9c9-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8f9c9-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f9c9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9c9-125">Funciones de formato de píxeles</span><span class="sxs-lookup"><span data-stu-id="8f9c9-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 




