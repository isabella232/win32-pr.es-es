---
description: Windows GDI+ es una API basada en clases para los programadores de C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154221"
---
# <a name="gdi"></a><span data-ttu-id="04033-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="04033-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="04033-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="04033-104">Purpose</span></span>

<span data-ttu-id="04033-105">Windows GDI+ es una API basada en clases para los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="04033-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="04033-106">Permite a las aplicaciones utilizar gráficos y texto con formato tanto en la pantalla de vídeo como en la impresora.</span><span class="sxs-lookup"><span data-stu-id="04033-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="04033-107">Las aplicaciones basadas en la API de Microsoft Win32 no tienen acceso al hardware gráfico directamente.</span><span class="sxs-lookup"><span data-stu-id="04033-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="04033-108">En su lugar, GDI+ interactúa con controladores de dispositivo en nombre de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="04033-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="04033-109">GDI+ también es compatible con Microsoft Win64.</span><span class="sxs-lookup"><span data-stu-id="04033-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="04033-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="04033-110">Where applicable</span></span>

<span data-ttu-id="04033-111">Las funciones y clases GDI+ no se admiten para su uso en un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="04033-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="04033-112">El intento de usar estas funciones y clases de un servicio de Windows puede producir problemas inesperados, como el rendimiento reducido del servicio y las excepciones o errores en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="04033-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="04033-113">Cuando se usa la API GDI+, nunca se debe permitir que la aplicación Descargue fuentes arbitrarias de orígenes que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="04033-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="04033-114">El sistema operativo requiere privilegios elevados para asegurarse de que todas las fuentes instaladas son de confianza.</span><span class="sxs-lookup"><span data-stu-id="04033-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="04033-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="04033-115">Developer audience</span></span>

<span data-ttu-id="04033-116">La interfaz basada en clases de C++ de GDI+ está diseñada para que la utilicen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="04033-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="04033-117">Es necesario estar familiarizado con la interfaz gráfica de usuario de Windows y la arquitectura controlada por mensajes.</span><span class="sxs-lookup"><span data-stu-id="04033-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="04033-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="04033-118">Run-time requirements</span></span>

<span data-ttu-id="04033-119">GDI+ se puede usar en todas las aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="04033-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="04033-120">GDI+ se presentó en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="04033-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="04033-121">Para obtener información sobre los sistemas operativos necesarios para usar una clase o un método determinados, vea la sección más información de la documentación de la clase o el método.</span><span class="sxs-lookup"><span data-stu-id="04033-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04033-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="04033-122">In this section</span></span>

| <span data-ttu-id="04033-123">Tema</span><span class="sxs-lookup"><span data-stu-id="04033-123">Topic</span></span>                                                    | <span data-ttu-id="04033-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="04033-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="04033-125">Información general</span><span class="sxs-lookup"><span data-stu-id="04033-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="04033-126">Información general sobre GDI+.</span><span class="sxs-lookup"><span data-stu-id="04033-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="04033-127">Utilizan</span><span class="sxs-lookup"><span data-stu-id="04033-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="04033-128">Tareas y ejemplos con GDI+.</span><span class="sxs-lookup"><span data-stu-id="04033-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="04033-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="04033-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="04033-130">Documentación de la API basada en clases de C++ de GDI+.</span><span class="sxs-lookup"><span data-stu-id="04033-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="04033-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04033-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04033-132">GDI de Windows</span><span class="sxs-lookup"><span data-stu-id="04033-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="04033-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="04033-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="04033-134">Adquisición de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="04033-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="04033-135">OpenGL</span><span class="sxs-lookup"><span data-stu-id="04033-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="04033-136">Multimedia de Windows</span><span class="sxs-lookup"><span data-stu-id="04033-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
