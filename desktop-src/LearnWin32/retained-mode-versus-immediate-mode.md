---
title: Modo retenido frente al modo inmediato
description: Las API de gráficos pueden dividirse en API de modo retenido y API de modo inmediato.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104562158"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="4e495-103">Modo retenido frente al modo inmediato</span><span class="sxs-lookup"><span data-stu-id="4e495-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="4e495-104">Las API de gráficos pueden dividirse en API de *modo retenido* y API *de modo inmediato* .</span><span class="sxs-lookup"><span data-stu-id="4e495-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="4e495-105">Direct2D es una API de modo inmediato.</span><span class="sxs-lookup"><span data-stu-id="4e495-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="4e495-106">Windows Presentation Foundation (WPF) es un ejemplo de una API de modo retenido.</span><span class="sxs-lookup"><span data-stu-id="4e495-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="4e495-107">Una API de modo retenido es declarativo.</span><span class="sxs-lookup"><span data-stu-id="4e495-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="4e495-108">La aplicación crea una escena a partir de primitivas de gráficos, como formas y líneas.</span><span class="sxs-lookup"><span data-stu-id="4e495-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="4e495-109">La biblioteca de gráficos almacena un modelo de la escena en la memoria.</span><span class="sxs-lookup"><span data-stu-id="4e495-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="4e495-110">Para dibujar un marco, la biblioteca de gráficos transforma la escena en un conjunto de comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="4e495-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="4e495-111">Entre fotogramas, la biblioteca de gráficos mantiene la escena en memoria.</span><span class="sxs-lookup"><span data-stu-id="4e495-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="4e495-112">Para cambiar lo que se representa, la aplicación emite un comando para actualizar la escena, por ejemplo, para agregar o quitar una forma.</span><span class="sxs-lookup"><span data-stu-id="4e495-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="4e495-113">A continuación, la biblioteca es responsable de volver a dibujar la escena.</span><span class="sxs-lookup"><span data-stu-id="4e495-113">The library is then responsible for redrawing the scene.</span></span>

![diagrama que muestra los gráficos en modo retenido.](images/graphics06.png)

<span data-ttu-id="4e495-115">Una API de modo inmediato es un procedimiento.</span><span class="sxs-lookup"><span data-stu-id="4e495-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="4e495-116">Cada vez que se dibuja un nuevo fotograma, la aplicación emite directamente los comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="4e495-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="4e495-117">La biblioteca de gráficos no almacena un modelo de escena entre fotogramas.</span><span class="sxs-lookup"><span data-stu-id="4e495-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="4e495-118">En su lugar, la aplicación realiza un seguimiento de la escena.</span><span class="sxs-lookup"><span data-stu-id="4e495-118">Instead, the application keeps track of the scene.</span></span>

![diagrama que muestra los gráficos en modo inmediato.](images/graphics07.png)

<span data-ttu-id="4e495-120">Las API de modo retenido pueden ser más fáciles de usar, ya que la API hace más trabajo para usted, como la inicialización, el mantenimiento del estado y la limpieza.</span><span class="sxs-lookup"><span data-stu-id="4e495-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="4e495-121">Por otro lado, suelen ser menos flexibles, ya que la API impone su propio modelo de escena.</span><span class="sxs-lookup"><span data-stu-id="4e495-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="4e495-122">Además, una API de modo retenido puede tener más requisitos de memoria, ya que debe proporcionar un modelo de escena de uso general.</span><span class="sxs-lookup"><span data-stu-id="4e495-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="4e495-123">Con una API de modo inmediato, puede implementar optimizaciones de destino.</span><span class="sxs-lookup"><span data-stu-id="4e495-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="4e495-124">Siguientes</span><span class="sxs-lookup"><span data-stu-id="4e495-124">Next</span></span>

[<span data-ttu-id="4e495-125">Su primer programa de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4e495-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 




