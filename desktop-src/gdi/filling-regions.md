---
description: Una aplicación rellena el interior de una región llamando a la función FillRgn y proporcionando un identificador que identifica un pincel específico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Rellenar regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082358"
---
# <a name="filling-regions"></a><span data-ttu-id="8dd65-103">Rellenar regiones</span><span class="sxs-lookup"><span data-stu-id="8dd65-103">Filling Regions</span></span>

<span data-ttu-id="8dd65-104">Una aplicación rellena el interior de una región llamando a la función [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) y proporcionando un identificador que identifica un pincel específico.</span><span class="sxs-lookup"><span data-stu-id="8dd65-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="8dd65-105">Cuando una aplicación llama a FillRgn, el sistema rellena la región con el pincel usando el modo de relleno actual para el contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8dd65-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="8dd65-106">Hay dos modos de relleno: alternativo y bobinado.</span><span class="sxs-lookup"><span data-stu-id="8dd65-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="8dd65-107">La aplicación puede establecer el modo de relleno para un contexto de dispositivo mediante una llamada a la función [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="8dd65-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="8dd65-108">La aplicación puede recuperar el modo de relleno actual para un contexto de dispositivo mediante una llamada a la función [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="8dd65-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="8dd65-109">En la ilustración siguiente se muestran dos regiones idénticas: una rellenada con el modo alternativo y la otra rellenada con el modo de bobinado.</span><span class="sxs-lookup"><span data-stu-id="8dd65-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![Ilustración en la que se muestran estrellas 2 5: una rellena solo en los puntos, el otro relleno completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="8dd65-111">Modo alternativo</span><span class="sxs-lookup"><span data-stu-id="8dd65-111">Alternate Mode</span></span>

<span data-ttu-id="8dd65-112">Para determinar qué píxeles resalta el sistema cuando se especifica el modo alternativo, realice la siguiente prueba:</span><span class="sxs-lookup"><span data-stu-id="8dd65-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="8dd65-113">Seleccione un píxel dentro del interior de la región.</span><span class="sxs-lookup"><span data-stu-id="8dd65-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="8dd65-114">Dibuja un rayo imaginario, en la dirección x positiva, desde ese píxel hasta el infinito.</span><span class="sxs-lookup"><span data-stu-id="8dd65-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="8dd65-115">Cada vez que el rayo intersecta con una línea de límite, incrementa un valor de recuento.</span><span class="sxs-lookup"><span data-stu-id="8dd65-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="8dd65-116">El sistema resalta el píxel si el valor de recuento es un número impar.</span><span class="sxs-lookup"><span data-stu-id="8dd65-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="8dd65-117">Modo de bobinado</span><span class="sxs-lookup"><span data-stu-id="8dd65-117">Winding Mode</span></span>

<span data-ttu-id="8dd65-118">Para determinar qué píxeles resalta el sistema cuando se especifica el modo de bobinado, realice la siguiente prueba:</span><span class="sxs-lookup"><span data-stu-id="8dd65-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="8dd65-119">Determine la dirección en la que se dibuja cada línea de límite.</span><span class="sxs-lookup"><span data-stu-id="8dd65-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="8dd65-120">Seleccione un píxel dentro del interior de la región.</span><span class="sxs-lookup"><span data-stu-id="8dd65-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="8dd65-121">Dibuja un rayo imaginario, en la dirección x positiva, desde el píxel hasta el infinito.</span><span class="sxs-lookup"><span data-stu-id="8dd65-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="8dd65-122">Cada vez que el rayo intersecta con una línea de límite con un componente y positivo, incrementa un valor de recuento.</span><span class="sxs-lookup"><span data-stu-id="8dd65-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="8dd65-123">Cada vez que el rayo intersecta con una línea de límite con un componente y negativo, disminuye el valor de recuento.</span><span class="sxs-lookup"><span data-stu-id="8dd65-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="8dd65-124">El sistema resalta el píxel si el valor de recuento es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8dd65-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



