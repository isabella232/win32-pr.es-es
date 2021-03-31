---
title: API de ampliación
description: La API de ampliación permite a las aplicaciones ampliar toda la pantalla o partes de la pantalla y aplicar efectos de color.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2020
ms.locfileid: "103904388"
---
# <a name="magnification-api"></a><span data-ttu-id="4f8ab-103">API de ampliación</span><span class="sxs-lookup"><span data-stu-id="4f8ab-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="4f8ab-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="4f8ab-104">Purpose</span></span>

<span data-ttu-id="4f8ab-105">La API de ampliación permite a las aplicaciones ampliar toda la pantalla o partes de la pantalla y aplicar efectos de color.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="4f8ab-106">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="4f8ab-106">Where applicable</span></span>

<span data-ttu-id="4f8ab-107">Mediante el uso de la API de ampliación, los desarrolladores pueden crear aplicaciones de tecnología de asistencia basadas en Windows que amplían la pantalla y aplican efectos de color al contenido de la pantalla ampliada.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="4f8ab-108">En el caso de los usuarios con poca visión, el tamaño de imagen y los efectos de color más grandes pueden facilitar la visualización y el uso del equipo.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4f8ab-109">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="4f8ab-109">Developer audience</span></span>

<span data-ttu-id="4f8ab-110">La API de ampliación está diseñada principalmente para desarrolladores de C y C++ que entienden la programación de Windows y que están familiarizados con los conceptos de programación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4f8ab-111">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4f8ab-111">Run-time requirements</span></span>

<span data-ttu-id="4f8ab-112">La versión inicial de la API de ampliación es compatible con Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="4f8ab-113">Una segunda versión agrega capacidades de ampliación de pantalla completa y se admite en Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="4f8ab-114">La API es compatible con Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="4f8ab-115">Para compilar la aplicación, incluya proprof. h y vincule a Amplification. lib.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="4f8ab-116">La API de ampliación no se admite en WOW64; es decir, una aplicación del ampliador de 32 bits no se ejecutará correctamente en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f8ab-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4f8ab-117">In this section</span></span>

| <span data-ttu-id="4f8ab-118">Tema</span><span class="sxs-lookup"><span data-stu-id="4f8ab-118">Topic</span></span> | <span data-ttu-id="4f8ab-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f8ab-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="4f8ab-120">Introducción a la API de ampliación</span><span class="sxs-lookup"><span data-stu-id="4f8ab-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="4f8ab-121">En este tema se describe la API de ampliación y se explica cómo utilizarla en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="4f8ab-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="4f8ab-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="4f8ab-123">Esta sección contiene información de referencia de la API de ampliación.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="4f8ab-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4f8ab-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="4f8ab-125">En la aplicación de ejemplo siguiente se muestra cómo usar la API de ampliación para crear un ampliador de pantalla completa que amplía toda la pantalla y un ampliador en ventanas que amplía y muestra una parte de la pantalla en una ventana.</span><span class="sxs-lookup"><span data-stu-id="4f8ab-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="4f8ab-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f8ab-126">Related topics</span></span>

<span data-ttu-id="4f8ab-127">[Sitio web de accesibilidad de Microsoft](https://www.microsoft.com/accessibility/), [accesibilidad en Windows 10](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="4f8ab-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>
