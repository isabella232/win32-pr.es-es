---
title: Sistema de colores de Windows
description: Los esquemas de administración del color se implementan en los sistemas operativos Microsoft Windows para mejorar la representación del contenido de color en todas las formas de comunicación digital. El esquema de administración del color que se usa a partir de Windows 2000, Windows XP y Windows Server 2003 se denomina administración del color de imagen (ICM) 2,0. El esquema de administración del color que se usa a partir de Windows Vista se denomina sistema de color de Windows (WCS) 1,0. El esquema de administración del color WCS 1,0 es un superconjunto de API y funcionalidad de ICM 2,0.
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721373"
---
# <a name="windows-color-system"></a><span data-ttu-id="6ed6a-105">Sistema de colores de Windows</span><span class="sxs-lookup"><span data-stu-id="6ed6a-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="6ed6a-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="6ed6a-106">Purpose</span></span>

<span data-ttu-id="6ed6a-107">Los esquemas de administración del color se implementan en los sistemas operativos Microsoft Windows para mejorar la representación del contenido de color en todas las formas de comunicación digital.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="6ed6a-108">El esquema de administración del color que se usa a partir de Windows 2000, Windows XP y Windows Server 2003 se denomina administración del color de imagen (ICM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="6ed6a-109">El esquema de administración del color que se usa a partir de Windows Vista se denomina sistema de color de Windows (WCS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="6ed6a-110">El esquema de administración del color WCS 1,0 es un superconjunto de API y funcionalidad de ICM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6ed6a-111">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="6ed6a-111">Where applicable</span></span>

<span data-ttu-id="6ed6a-112">ICM se puede usar en todas las aplicaciones de Windows 2000 y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="6ed6a-113">WCS se puede usar en todas las aplicaciones de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6ed6a-114">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="6ed6a-114">Developer audience</span></span>

<span data-ttu-id="6ed6a-115">La API WCS está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="6ed6a-116">Es necesario estar familiarizado con la interfaz gráfica de usuario de Windows, la arquitectura controlada por mensajes y el conocimiento práctico de los conceptos de administración del color.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6ed6a-117">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="6ed6a-117">Run-time requirements</span></span>

<span data-ttu-id="6ed6a-118">Las aplicaciones que usan la API de ICM requieren Windows 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="6ed6a-119">Las aplicaciones que usan la API WCS requieren Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="6ed6a-120">Para obtener información específica sobre el tiempo de ejecución de una función, consulte la sección requisitos de la página de referencia de esa función.</span><span class="sxs-lookup"><span data-stu-id="6ed6a-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6ed6a-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6ed6a-121">In this section</span></span>

-   [<span data-ttu-id="6ed6a-122">Consideraciones de seguridad: sistema de color de Windows</span><span class="sxs-lookup"><span data-stu-id="6ed6a-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="6ed6a-123">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="6ed6a-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="6ed6a-124">Algoritmos y esquemas del Sistema de colores de Windows</span><span class="sxs-lookup"><span data-stu-id="6ed6a-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="6ed6a-125">Acerca del Sistema de colores de Windows, versión 1.0</span><span class="sxs-lookup"><span data-stu-id="6ed6a-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="6ed6a-126">Uso de WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="6ed6a-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="6ed6a-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="6ed6a-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="6ed6a-128">Glosario de WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="6ed6a-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="6ed6a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ed6a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed6a-130">OpenGL</span><span class="sxs-lookup"><span data-stu-id="6ed6a-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="6ed6a-131">Multimedia de Windows</span><span class="sxs-lookup"><span data-stu-id="6ed6a-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="6ed6a-132">GDI de Windows</span><span class="sxs-lookup"><span data-stu-id="6ed6a-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 