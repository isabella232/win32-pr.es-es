---
title: Programar un guion gráfico
description: Una vez creado un guion gráfico, lo programa el administrador de animaciones.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- guiones gráficos animación y programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075163"
---
# <a name="schedule-a-storyboard"></a><span data-ttu-id="a30dd-104">Programar un guion gráfico</span><span class="sxs-lookup"><span data-stu-id="a30dd-104">Schedule a Storyboard</span></span>

<span data-ttu-id="a30dd-105">Una vez creado un guion gráfico, lo programa el administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="a30dd-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="a30dd-106">Información general</span><span class="sxs-lookup"><span data-stu-id="a30dd-106">Overview</span></span>

<span data-ttu-id="a30dd-107">De forma predeterminada, cada guion gráfico se inicia inmediatamente cuando está programado.</span><span class="sxs-lookup"><span data-stu-id="a30dd-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="a30dd-108">Esto significa que cuando un guion gráfico comienza a animar una o más variables, puede interrumpir cualquier otro guion gráfico que anime esas mismas variables.</span><span class="sxs-lookup"><span data-stu-id="a30dd-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="a30dd-109">Sin embargo, una aplicación puede especificar otros comportamientos determinando la prioridad relativa entre los guiones gráficos.</span><span class="sxs-lookup"><span data-stu-id="a30dd-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="a30dd-110">Una vez que se ha programado un guion gráfico, ya no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="a30dd-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="a30dd-111">Sin embargo, una vez que se ha quitado un guion gráfico de la programación, se puede programar para que se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="a30dd-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="a30dd-112">Los desarrolladores deben tener cuidado al volver a usar guiones gráficos, ya que esto solo debe hacerse cuando no es posible que sea necesario poner en cola el mismo guion gráfico debido a una acción del usuario cuando ya se está reproduciendo o en cola en la programación.</span><span class="sxs-lookup"><span data-stu-id="a30dd-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="a30dd-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a30dd-113">Example Code</span></span>

<span data-ttu-id="a30dd-114">El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplos de animaciones [controladas](application-driven-animation-sample.md) por la aplicación y la [animación controlada por temporizador](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a30dd-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="a30dd-115">Usa el método [**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) para programar el guión gráfico.</span><span class="sxs-lookup"><span data-stu-id="a30dd-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="a30dd-116">Este método requiere la hora actual como parámetro.</span><span class="sxs-lookup"><span data-stu-id="a30dd-116">This method requires the current time as a parameter.</span></span>


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a><span data-ttu-id="a30dd-117">Paso anterior</span><span class="sxs-lookup"><span data-stu-id="a30dd-117">Previous Step</span></span>

<span data-ttu-id="a30dd-118">Antes de comenzar este paso, debe haber completado este paso: [crear un guion gráfico y agregar transiciones](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="a30dd-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a30dd-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a30dd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a30dd-120">**IUIAnimationStoryboard:: Schedule**</span><span class="sxs-lookup"><span data-stu-id="a30dd-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="a30dd-121">**IUIAnimationTimer:: GetTime**</span><span class="sxs-lookup"><span data-stu-id="a30dd-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="a30dd-122">Información general sobre guiones gráficos</span><span class="sxs-lookup"><span data-stu-id="a30dd-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




