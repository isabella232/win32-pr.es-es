---
title: Crear variables de animación
description: Una aplicación debe crear una variable de animación para cada característica de visual que se va a animar mediante la animación de Windows.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- variables de animación animación de Windows, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421225"
---
# <a name="create-animation-variables"></a><span data-ttu-id="3bae7-104">Crear variables de animación</span><span class="sxs-lookup"><span data-stu-id="3bae7-104">Create Animation Variables</span></span>

<span data-ttu-id="3bae7-105">Una aplicación debe crear una variable de animación para cada característica de visual que se va a animar mediante la animación de Windows.</span><span class="sxs-lookup"><span data-stu-id="3bae7-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="3bae7-106">Información general</span><span class="sxs-lookup"><span data-stu-id="3bae7-106">Overview</span></span>

<span data-ttu-id="3bae7-107">Las variables de animación se crean mediante el administrador de animaciones y la aplicación debe conservar una referencia a cada para siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3bae7-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="3bae7-108">Normalmente, la aplicación creará cada variable de animación al mismo tiempo que el objeto visual que anima.</span><span class="sxs-lookup"><span data-stu-id="3bae7-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="3bae7-109">Cuando se crea una variable de animación, se debe especificar su valor inicial.</span><span class="sxs-lookup"><span data-stu-id="3bae7-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="3bae7-110">Después, su valor solo puede modificarse mediante la programación de guiones gráficos que lo animan.</span><span class="sxs-lookup"><span data-stu-id="3bae7-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="3bae7-111">Las variables de animación se pasan como parámetros cuando se construyen guiones gráficos, por lo que la aplicación no debe liberarlas hasta que no sea necesario animar las características visuales que representan, normalmente cuando los objetos visuales asociados están a punto de ser destruidos.</span><span class="sxs-lookup"><span data-stu-id="3bae7-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="3bae7-112">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bae7-112">Example Code</span></span>

-   [<span data-ttu-id="3bae7-113">Animar colores</span><span class="sxs-lookup"><span data-stu-id="3bae7-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="3bae7-114">Animar coordenadas x e y</span><span class="sxs-lookup"><span data-stu-id="3bae7-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="3bae7-115">Animar colores</span><span class="sxs-lookup"><span data-stu-id="3bae7-115">Animating Colors</span></span>

<span data-ttu-id="3bae7-116">El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplos de animaciones [controladas](application-driven-animation-sample.md) por la aplicación y la [animación controlada por temporizador](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3bae7-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="3bae7-117">En el ejemplo, se crean tres variables de animación mediante [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) para representar los colores de fondo.</span><span class="sxs-lookup"><span data-stu-id="3bae7-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="3bae7-118">El código también usa los métodos [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) y [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) para controlar el valor de la variable de animación.</span><span class="sxs-lookup"><span data-stu-id="3bae7-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



<span data-ttu-id="3bae7-119">Tenga en cuenta las siguientes definiciones de MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="3bae7-119">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="3bae7-120">Animar coordenadas x e y</span><span class="sxs-lookup"><span data-stu-id="3bae7-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="3bae7-121">El siguiente código de ejemplo se toma de thumbnail. cpp en el [ejemplo de diseño de cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample)de animación de Windows. Vea el método CMainWindow:: CreateAnimationVariables.</span><span class="sxs-lookup"><span data-stu-id="3bae7-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="3bae7-122">Se crean dos variables de animación para representar las coordenadas X e y de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="3bae7-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



<span data-ttu-id="3bae7-123">Tenga en cuenta las siguientes definiciones de thumbnail. h.</span><span class="sxs-lookup"><span data-stu-id="3bae7-123">Note the following definitions from Thumbnail.h.</span></span>


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



<span data-ttu-id="3bae7-124">Las variables de animación son números de punto flotante, pero sus valores también se pueden capturar como enteros.</span><span class="sxs-lookup"><span data-stu-id="3bae7-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="3bae7-125">De forma predeterminada, cada valor se redondea al entero más próximo, pero es posible invalidar el modo de redondeo que se usa para una variable.</span><span class="sxs-lookup"><span data-stu-id="3bae7-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="3bae7-126">En el ejemplo de código siguiente se usa el método [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) para especificar que los valores siempre se deben redondear hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="3bae7-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="3bae7-127">Paso anterior</span><span class="sxs-lookup"><span data-stu-id="3bae7-127">Previous Step</span></span>

<span data-ttu-id="3bae7-128">Antes de comenzar este paso, debe haber completado este paso: [crear los objetos de animación principales](adding-animation-to-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="3bae7-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="3bae7-129">siguiente paso</span><span class="sxs-lookup"><span data-stu-id="3bae7-129">Next Step</span></span>

<span data-ttu-id="3bae7-130">Después de completar este paso, el paso siguiente es [actualizar el administrador de animaciones y dibujar fotogramas](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3bae7-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bae7-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3bae7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bae7-132">**IUIAnimationManager::CreateAnimationVariable**</span><span class="sxs-lookup"><span data-stu-id="3bae7-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="3bae7-133">**IUIAnimationVariable::SetLowerBound**</span><span class="sxs-lookup"><span data-stu-id="3bae7-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="3bae7-134">**IUIAnimationVariable::SetRoundingMode**</span><span class="sxs-lookup"><span data-stu-id="3bae7-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="3bae7-135">**IUIAnimationVariable::SetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="3bae7-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="3bae7-136">Información general sobre animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="3bae7-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 