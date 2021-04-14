---
title: OpenGL
description: Como interfaz de software para el hardware de gráficos, OpenGL representa los objetos multidimensionales en un fotogramas.
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488186"
---
# <a name="opengl"></a><span data-ttu-id="ed0c4-103">OpenGL</span><span class="sxs-lookup"><span data-stu-id="ed0c4-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="ed0c4-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="ed0c4-104">Purpose</span></span>

<span data-ttu-id="ed0c4-105">Como interfaz de software para el hardware de gráficos, OpenGL representa los objetos multidimensionales en un fotogramas.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="ed0c4-106">La implementación de OpenGL de Microsoft para el sistema operativo Windows es un software de gráficos estándar del sector con el que los programadores pueden crear imágenes de color tridimensionales aún y animadas de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="ed0c4-107">La versión de OpenGL descrita en esta sección es 1,1.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="ed0c4-108">Para obtener información sobre OpenGL ES que se ejecuta en Windows, consulte [ángulo de la tienda Windows](https://github.com/microsoft/angle/wiki).</span><span class="sxs-lookup"><span data-stu-id="ed0c4-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="ed0c4-109">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="ed0c4-109">Where applicable</span></span>

<span data-ttu-id="ed0c4-110">OpenGL se ha creado para ofrecer compatibilidad entre hardware y sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="ed0c4-111">Esta arquitectura facilita el traslado de programas OpenGL de un sistema a otro.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="ed0c4-112">Aunque cada sistema operativo tiene requisitos únicos, el código OpenGL de muchos programas se puede usar tal cual.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ed0c4-113">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="ed0c4-113">Developer audience</span></span>

<span data-ttu-id="ed0c4-114">OpenGL, diseñado para que lo usen los programadores de C/C++, debe estar familiarizado con la interfaz gráfica de usuario de Windows, así como con la arquitectura orientada a mensajes.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ed0c4-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ed0c4-115">Run-time requirements</span></span>

<span data-ttu-id="ed0c4-116">Para obtener más información sobre los sistemas operativos necesarios para una función determinada, consulte la sección de requisitos de la documentación de la función.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed0c4-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ed0c4-117">In this section</span></span>



| <span data-ttu-id="ed0c4-118">Tema</span><span class="sxs-lookup"><span data-stu-id="ed0c4-118">Topic</span></span>                                             | <span data-ttu-id="ed0c4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed0c4-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed0c4-120">Información general</span><span class="sxs-lookup"><span data-stu-id="ed0c4-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="ed0c4-121">Información general sobre el funcionamiento de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="ed0c4-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="ed0c4-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="ed0c4-123">Documentación de funciones, estructuras y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="ed0c4-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed0c4-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="ed0c4-125">Ejemplos de código OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ed0c4-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="ed0c4-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed0c4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed0c4-127">Gráficos y juegos de DirectX</span><span class="sxs-lookup"><span data-stu-id="ed0c4-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="ed0c4-128">[Imagen estática](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed0c4-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ed0c4-129">[Sistema de color de Windows (WCS)](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed0c4-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ed0c4-130">GDI de Windows</span><span class="sxs-lookup"><span data-stu-id="ed0c4-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="ed0c4-131">Adquisición de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="ed0c4-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="ed0c4-132">Multimedia de Windows</span><span class="sxs-lookup"><span data-stu-id="ed0c4-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="ed0c4-133">[API de Windows](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed0c4-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

