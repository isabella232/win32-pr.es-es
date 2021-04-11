---
description: Un contexto de dispositivo (DC) es una estructura de datos que define los objetos gráficos, sus atributos asociados y los modos gráficos que afectan a la salida en un dispositivo. Para crear un controlador de dominio, llame a la función CreateDC. para recuperar un controlador de dominio, llame a la función GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Mapas de bits, contextos de dispositivo y superficies de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276022"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="153c0-104">Mapas de bits, contextos de dispositivo y superficies de dibujo</span><span class="sxs-lookup"><span data-stu-id="153c0-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="153c0-105">Un *contexto de dispositivo* (DC) es una estructura de datos que define los objetos gráficos, sus atributos asociados y los modos gráficos que afectan a la salida en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="153c0-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="153c0-106">Para crear un controlador de dominio, llame a la función [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . para recuperar un controlador de dominio, llame a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="153c0-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="153c0-107">Antes de devolver un identificador que identifica ese DC, el sistema selecciona una superficie de dibujo en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="153c0-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="153c0-108">Si la aplicación llamó a la función [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) para crear un contexto de dispositivo para una pantalla VGA, las dimensiones de esta superficie de dibujo son de 640 a 480 píxeles.</span><span class="sxs-lookup"><span data-stu-id="153c0-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="153c0-109">Si la aplicación ha llamado a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , las dimensiones reflejan el tamaño del área cliente.</span><span class="sxs-lookup"><span data-stu-id="153c0-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="153c0-110">Antes de que una aplicación pueda comenzar a dibujar, debe seleccionar un mapa de bits con el ancho y el alto adecuados en el controlador de dominio mediante una llamada a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="153c0-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="153c0-111">Cuando una aplicación pasa el identificador al controlador de dominio a una de las funciones de dibujo de la interfaz de dispositivo gráfico (GDI), la salida solicitada aparece en la superficie de dibujo seleccionada en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="153c0-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="153c0-112">Para obtener más información, vea [contextos de dispositivo de memoria](memory-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="153c0-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



