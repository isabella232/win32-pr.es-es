---
title: Usar contextos de dispositivo
description: Usar contextos de dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- visualizaciones, contexto de dispositivo
- visualizaciones personalizadas, contexto de dispositivo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357237"
---
# <a name="using-device-contexts"></a><span data-ttu-id="09f29-108">Usar contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="09f29-108">Using Device Contexts</span></span>

<span data-ttu-id="09f29-109">El contexto de dispositivo es un identificador estándar de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09f29-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="09f29-110">Lo necesita para muchas funciones de dibujo para que Microsoft Windows sepa en qué ventana se debe dibujar.</span><span class="sxs-lookup"><span data-stu-id="09f29-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="09f29-111">Por ejemplo, para dibujar un rectángulo, debe especificar el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09f29-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="09f29-112">Windows Media Player especifica el contexto del dispositivo a través de la función **Render** .</span><span class="sxs-lookup"><span data-stu-id="09f29-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="09f29-113">Si el complemento se representa mediante una ventana, deberá usar el contexto de dispositivo de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="09f29-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="09f29-114">Use este contexto de dispositivo para cualquier herramienta de dibujo que requiera un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09f29-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09f29-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09f29-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09f29-116">**Implementación de render**</span><span class="sxs-lookup"><span data-stu-id="09f29-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




