---
title: Leer los valores de las variables de animación
description: Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se van a animar.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variables de animación animación de Windows, lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695690"
---
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="c13c5-104">Leer los valores de las variables de animación</span><span class="sxs-lookup"><span data-stu-id="c13c5-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="c13c5-105">Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se van a animar.</span><span class="sxs-lookup"><span data-stu-id="c13c5-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="c13c5-106">Información general</span><span class="sxs-lookup"><span data-stu-id="c13c5-106">Overview</span></span>

<span data-ttu-id="c13c5-107">Al dibujar un marco, una aplicación puede usar el método [**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) o [**IUIAnimationVariable:: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para solicitar los valores de cualquier variable de animación que afecte a los objetos visuales del marco.</span><span class="sxs-lookup"><span data-stu-id="c13c5-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="c13c5-108">Es posible recortar una variable de animación a un intervalo de valores ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) y [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) y solicitar que su valor se redondee a un entero mediante un esquema de redondeo especificado ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span><span class="sxs-lookup"><span data-stu-id="c13c5-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="c13c5-109">En lugar de leer los valores de todas las variables de cada fotograma, una aplicación puede usar el método [**IUIAnimationVariable:: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) o [**IUIAnimationVariable:: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) para registrar uno o más controladores de cambios de variable para recibir notificaciones solo cuando se produce un cambio en el valor de las variables ([**IUIAnimationVariableChangeHandler:: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) o un valor redondeado ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span><span class="sxs-lookup"><span data-stu-id="c13c5-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="c13c5-110">Para identificar las variables que se pasan a los controladores de cambios de variable, una aplicación puede aplicar etiquetas a las variables mediante el método [**IUIAnimationVariable:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) .</span><span class="sxs-lookup"><span data-stu-id="c13c5-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="c13c5-111">Estos son objetos (IUnknown \* ), pares de enteros que se interpretan por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c13c5-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="c13c5-112">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c13c5-112">Example Code</span></span>

<span data-ttu-id="c13c5-113">El siguiente código de ejemplo se toma de thumbnail. cpp en el diseño de [cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample)de ejemplo de animación de Windows. Vea el método CMainWindow:: Render.</span><span class="sxs-lookup"><span data-stu-id="c13c5-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="c13c5-114">Usa el método [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) para leer los valores como valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="c13c5-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



<span data-ttu-id="c13c5-115">El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplo de animación [controlada por temporizador](timer-driven-animation-sample.md); Vea el método CMainWindow::D rawBackground.</span><span class="sxs-lookup"><span data-stu-id="c13c5-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="c13c5-116">Usa el método [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para leer los valores como valores enteros.</span><span class="sxs-lookup"><span data-stu-id="c13c5-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="c13c5-117">Paso anterior</span><span class="sxs-lookup"><span data-stu-id="c13c5-117">Previous Step</span></span>

<span data-ttu-id="c13c5-118">Antes de comenzar este paso, debe haber completado este paso: [actualizar el administrador de animaciones y dibujar Marcos](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="c13c5-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="c13c5-119">siguiente paso</span><span class="sxs-lookup"><span data-stu-id="c13c5-119">Next Step</span></span>

<span data-ttu-id="c13c5-120">Después de completar este paso, el paso siguiente es [crear un guión gráfico y agregar transiciones](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="c13c5-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c13c5-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c13c5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c13c5-122">**IUIAnimationVariable::GetIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="c13c5-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="c13c5-123">**IUIAnimationVariable:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="c13c5-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="c13c5-124">Información general sobre animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="c13c5-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 