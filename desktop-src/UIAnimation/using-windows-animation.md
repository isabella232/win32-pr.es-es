---
title: Tareas de animación de Windows
description: En los temas incluidos en esta sección se describen las tareas básicas necesarias para las aplicaciones que utilizan el administrador de animaciones de Windows.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animación de Windows animación de Windows, tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695436"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="6a20d-104">Tareas de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="6a20d-104">Windows Animation Tasks</span></span>

<span data-ttu-id="6a20d-105">En los temas incluidos en esta sección se describen las tareas básicas necesarias para las aplicaciones que utilizan el administrador de animaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a20d-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="6a20d-106">Estas tareas, en orden, incluyen:</span><span class="sxs-lookup"><span data-stu-id="6a20d-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6a20d-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6a20d-107">In this section</span></span>



| <span data-ttu-id="6a20d-108">Tema</span><span class="sxs-lookup"><span data-stu-id="6a20d-108">Topic</span></span>                                                                                                | <span data-ttu-id="6a20d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a20d-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a20d-110">Crear los objetos de animación principales</span><span class="sxs-lookup"><span data-stu-id="6a20d-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="6a20d-111">Para usar la animación de Windows en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.</span><span class="sxs-lookup"><span data-stu-id="6a20d-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="6a20d-112">Crear variables de animación</span><span class="sxs-lookup"><span data-stu-id="6a20d-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="6a20d-113">Una aplicación debe crear una variable de animación para cada característica de visual que se va a animar mediante la animación de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a20d-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="6a20d-114">Actualizar el administrador de animaciones y dibujar marcos</span><span class="sxs-lookup"><span data-stu-id="6a20d-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="6a20d-115">Cada vez que una aplicación programa un guion gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="6a20d-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="6a20d-116">También se requiere la hora actual al dirigir el administrador de animaciones para actualizar su estado y establecer todas las variables de animación en los valores interpolados adecuados.</span><span class="sxs-lookup"><span data-stu-id="6a20d-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="6a20d-117">Leer los valores de las variables de animación</span><span class="sxs-lookup"><span data-stu-id="6a20d-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="6a20d-118">Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se van a animar.</span><span class="sxs-lookup"><span data-stu-id="6a20d-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="6a20d-119">Crear un guion gráfico y agregar transiciones</span><span class="sxs-lookup"><span data-stu-id="6a20d-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="6a20d-120">Para crear una animación, una aplicación debe construir un guion gráfico.</span><span class="sxs-lookup"><span data-stu-id="6a20d-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="6a20d-121">Programar un guion gráfico</span><span class="sxs-lookup"><span data-stu-id="6a20d-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="6a20d-122">Una vez creado un guion gráfico, lo programa el administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="6a20d-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="6a20d-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a20d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a20d-124">Información general sobre animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="6a20d-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="6a20d-125">Referencia de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="6a20d-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="6a20d-126">Ejemplos de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="6a20d-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





