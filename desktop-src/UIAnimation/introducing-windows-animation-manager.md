---
title: Actualizar el administrador de animaciones y dibujar marcos
description: Cada vez que una aplicación programa un guion gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- objetos del administrador de animaciones animación de Windows, actualizar
- objetos de temporizador de animación animación de Windows, conectar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077852"
---
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="b341d-105">Actualizar el administrador de animaciones y dibujar marcos</span><span class="sxs-lookup"><span data-stu-id="b341d-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="b341d-106">Cada vez que una aplicación programa un guion gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="b341d-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="b341d-107">También se requiere la hora actual al dirigir el administrador de animaciones para actualizar su estado y establecer todas las variables de animación en los valores interpolados adecuados.</span><span class="sxs-lookup"><span data-stu-id="b341d-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="b341d-108">Información general</span><span class="sxs-lookup"><span data-stu-id="b341d-108">Overview</span></span>

<span data-ttu-id="b341d-109">Hay dos configuraciones admitidas por la animación de Windows: animación controlada por la aplicación y animación controlada por temporizador.</span><span class="sxs-lookup"><span data-stu-id="b341d-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="b341d-110">Para usar la animación controlada por la aplicación en la aplicación, debe actualizar el administrador de animaciones antes de dibujar cada fotograma y utilizar un mecanismo adecuado para dibujar fotogramas con la suficiente frecuencia para la animación.</span><span class="sxs-lookup"><span data-stu-id="b341d-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="b341d-111">Una aplicación que usa la animación controlada por la aplicación puede utilizar cualquier mecanismo para determinar la hora actual, pero el objeto de temporizador de animación de Windows devuelve una hora precisa en las unidades aceptadas por el administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="b341d-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="b341d-112">Para evitar dibujos innecesarios cuando no se reproducen animaciones, también debe proporcionar un controlador de eventos de administrador para iniciar la redibujado cuando se programan las animaciones y comprobar después de cada fotograma si se puede suspender el redibujo.</span><span class="sxs-lookup"><span data-stu-id="b341d-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="b341d-113">Para obtener más información, vea [animación controlada por la aplicación](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b341d-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="b341d-114">En la configuración controlada por aplicaciones, una aplicación puede llamar al método [**IUIAnimationManager:: getStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) para comprobar que las animaciones están programadas actualmente y continuar dibujando marcos si lo están.</span><span class="sxs-lookup"><span data-stu-id="b341d-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="b341d-115">Dado que volver a dibujar se detiene cuando no hay ninguna animación programada, es necesario reiniciarla la próxima vez que se programe una animación.</span><span class="sxs-lookup"><span data-stu-id="b341d-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="b341d-116">Una aplicación puede registrar un controlador de eventos de administrador para que se le notifique cuando el estado del administrador de animaciones cambie de inactivo (actualmente no hay animaciones programadas) a ocupado.</span><span class="sxs-lookup"><span data-stu-id="b341d-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="b341d-117">Para usar la animación controlada por temporizador en la aplicación, debe conectar el administrador de animaciones a un temporizador de animación y proporcionar un controlador de eventos Timer.</span><span class="sxs-lookup"><span data-stu-id="b341d-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="b341d-118">Cuando el administrador de animaciones está conectado a un temporizador, el temporizador puede indicar al administrador Cuándo debe actualizarse el estado de animación a medida que progresa el tiempo.</span><span class="sxs-lookup"><span data-stu-id="b341d-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="b341d-119">La aplicación debe dibujar un marco para cada paso del temporizador.</span><span class="sxs-lookup"><span data-stu-id="b341d-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="b341d-120">A su vez, el administrador de animaciones puede indicar al temporizador Cuándo se reproducen animaciones, por lo que el temporizador puede cerrarse durante los períodos de inactividad cuando no es necesario volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="b341d-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="b341d-121">Para evitar dibujos innecesarios cuando no se reproducen animaciones, debe configurar el temporizador para que se deshabilite automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b341d-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="b341d-122">Para obtener más información, vea [animación controlada por temporizador](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b341d-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="b341d-123">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b341d-123">Example Code</span></span>

-   [<span data-ttu-id="b341d-124">Animación controlada por aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b341d-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="b341d-125">Animación controlada por temporizador</span><span class="sxs-lookup"><span data-stu-id="b341d-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="b341d-126">Application-Driven animación</span><span class="sxs-lookup"><span data-stu-id="b341d-126">Application-Driven Animation</span></span>

<span data-ttu-id="b341d-127">El siguiente código de ejemplo se toma de ManagerEventHandler. h de [la animación de Windows ejemplos de](application-driven-animation-sample.md) animación y [diseño de cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample).</span><span class="sxs-lookup"><span data-stu-id="b341d-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="b341d-128">Define el controlador de eventos de administrador.</span><span class="sxs-lookup"><span data-stu-id="b341d-128">It defines the manager event handler.</span></span>


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



<span data-ttu-id="b341d-129">El siguiente código de ejemplo se toma de MainWindow. cpp de la animación de Windows de ejemplo Animation [orientada a la aplicación](application-driven-animation-sample.md). vea CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="b341d-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="b341d-130">En este ejemplo se crea una instancia del controlador de eventos Manager con el método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) y se pasa al administrador de animaciones mediante el método [**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="b341d-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



<span data-ttu-id="b341d-131">Dado que el controlador de eventos de administrador conserva una referencia al objeto de ventana principal, el controlador de eventos de administrador debe borrarse (pasando **null** a [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) o el administrador de animaciones debe liberarse por completo antes de que se destruya la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="b341d-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="b341d-132">El siguiente código de ejemplo se toma de MainWindow. cpp en la [animación de Windows de ejemplo animación controlada por la aplicación](application-driven-animation-sample.md); Vea el método CMainWindow:: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="b341d-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="b341d-133">Llama al método [**IUIAnimationManager:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) para recuperar la hora en las unidades requeridas por el método [**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .</span><span class="sxs-lookup"><span data-stu-id="b341d-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



<span data-ttu-id="b341d-134">El siguiente código de ejemplo se toma de MainWindow. cpp de la animación de Windows ejemplos de animación [orientada a la aplicación](application-driven-animation-sample.md) y el [diseño de cuadrículas](/windows/desktop/UIAnimation/grid-layout-sample). Vea el método CMainWindow:: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="b341d-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="b341d-135">Se supone que la aplicación está usando una API de gráficos que se sincroniza automáticamente con la frecuencia de actualización del monitor (como Direct2D con su configuración predeterminada), en cuyo caso una llamada a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) es suficiente para asegurarse de que se llamará de nuevo al código de dibujo cuando sea el momento de dibujar el fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="b341d-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="b341d-136">En lugar de llamar a **InvalidateRect** incondicionalmente, es mejor comprobar si todavía hay animaciones programadas mediante [**getStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span><span class="sxs-lookup"><span data-stu-id="b341d-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a><span data-ttu-id="b341d-137">Timer-Driven animación</span><span class="sxs-lookup"><span data-stu-id="b341d-137">Timer-Driven Animation</span></span>

<span data-ttu-id="b341d-138">El siguiente código de ejemplo se toma de TimerEventHandler. h de la animación de Windows de ejemplo Animation [controlada por temporizador](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b341d-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="b341d-139">El código de ejemplo define el controlador de eventos Timer, que invalida el área cliente de la ventana para que se vuelva a dibujar después de cada actualización del estado de la animación.</span><span class="sxs-lookup"><span data-stu-id="b341d-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



<span data-ttu-id="b341d-140">El siguiente código de ejemplo se toma de MainWindow. cpp de la animación de Windows de ejemplo Animation [controlada por temporizador](timer-driven-animation-sample.md); vea CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="b341d-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="b341d-141">En este ejemplo se crea una instancia del controlador de eventos Timer con el método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) y se pasa al temporizador mediante el método [**IUIAnimationTimer:: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="b341d-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="b341d-142">Dado que el controlador de eventos Timer conserva una referencia al objeto Window principal, el controlador de eventos Timer debe borrarse (pasando **null** a **SetTimerEventHandler**) o el temporizador completamente liberado antes de que se destruya la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="b341d-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



<span data-ttu-id="b341d-143">El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplo de animación [controlada por temporizador](timer-driven-animation-sample.md); Vea el método CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="b341d-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="b341d-144">Llama al método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto de administrador de animaciones para obtener un puntero a [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)y, a continuación, conecta los objetos [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) y [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) estableciendo el administrador de animaciones como el controlador de actualización del temporizador mediante el método [**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) .</span><span class="sxs-lookup"><span data-stu-id="b341d-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="b341d-145">Tenga en cuenta que no es necesario borrar explícitamente esta conexión; la conexión se borra de forma segura después de que la aplicación libera el administrador de animaciones y el temporizador de animación.</span><span class="sxs-lookup"><span data-stu-id="b341d-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



<span data-ttu-id="b341d-146">Si no se usa el **\_ \_ comportamiento de inactividad de animación \_ \_** de la interfaz de usuario, también es necesario habilitar el temporizador para iniciar la marcación.</span><span class="sxs-lookup"><span data-stu-id="b341d-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="b341d-147">Paso anterior</span><span class="sxs-lookup"><span data-stu-id="b341d-147">Previous Step</span></span>

<span data-ttu-id="b341d-148">Antes de comenzar este paso, debe haber completado este paso: [crear variables de animación](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="b341d-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="b341d-149">siguiente paso</span><span class="sxs-lookup"><span data-stu-id="b341d-149">Next Step</span></span>

<span data-ttu-id="b341d-150">Después de completar este paso, el paso siguiente es [leer los valores de la variable de animación](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="b341d-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b341d-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b341d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b341d-152">**IUIAnimationManager:: GetStatus**</span><span class="sxs-lookup"><span data-stu-id="b341d-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="b341d-153">**IUIAnimationManager::SetManagerEventHandler**</span><span class="sxs-lookup"><span data-stu-id="b341d-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="b341d-154">**IUIAnimationManager:: Update**</span><span class="sxs-lookup"><span data-stu-id="b341d-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="b341d-155">**IUIAnimationTimer:: GetTime**</span><span class="sxs-lookup"><span data-stu-id="b341d-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="b341d-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span><span class="sxs-lookup"><span data-stu-id="b341d-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="b341d-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b341d-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b341d-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b341d-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b341d-159">Información general sobre animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="b341d-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 