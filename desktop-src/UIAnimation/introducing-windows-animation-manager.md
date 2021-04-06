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
# <a name="update-the-animation-manager-and-draw-frames"></a>Actualizar el administrador de animaciones y dibujar marcos

Cada vez que una aplicación programa un guion gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones. También se requiere la hora actual al dirigir el administrador de animaciones para actualizar su estado y establecer todas las variables de animación en los valores interpolados adecuados.

## <a name="overview"></a>Información general

Hay dos configuraciones admitidas por la animación de Windows: animación controlada por la aplicación y animación controlada por temporizador.

Para usar la animación controlada por la aplicación en la aplicación, debe actualizar el administrador de animaciones antes de dibujar cada fotograma y utilizar un mecanismo adecuado para dibujar fotogramas con la suficiente frecuencia para la animación. Una aplicación que usa la animación controlada por la aplicación puede utilizar cualquier mecanismo para determinar la hora actual, pero el objeto de temporizador de animación de Windows devuelve una hora precisa en las unidades aceptadas por el administrador de animaciones. Para evitar dibujos innecesarios cuando no se reproducen animaciones, también debe proporcionar un controlador de eventos de administrador para iniciar la redibujado cuando se programan las animaciones y comprobar después de cada fotograma si se puede suspender el redibujo. Para obtener más información, vea [animación controlada por la aplicación](scenic-animation-api-overview.md).

En la configuración controlada por aplicaciones, una aplicación puede llamar al método [**IUIAnimationManager:: getStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) para comprobar que las animaciones están programadas actualmente y continuar dibujando marcos si lo están. Dado que volver a dibujar se detiene cuando no hay ninguna animación programada, es necesario reiniciarla la próxima vez que se programe una animación. Una aplicación puede registrar un controlador de eventos de administrador para que se le notifique cuando el estado del administrador de animaciones cambie de inactivo (actualmente no hay animaciones programadas) a ocupado.

Para usar la animación controlada por temporizador en la aplicación, debe conectar el administrador de animaciones a un temporizador de animación y proporcionar un controlador de eventos Timer. Cuando el administrador de animaciones está conectado a un temporizador, el temporizador puede indicar al administrador Cuándo debe actualizarse el estado de animación a medida que progresa el tiempo. La aplicación debe dibujar un marco para cada paso del temporizador. A su vez, el administrador de animaciones puede indicar al temporizador Cuándo se reproducen animaciones, por lo que el temporizador puede cerrarse durante los períodos de inactividad cuando no es necesario volver a dibujar. Para evitar dibujos innecesarios cuando no se reproducen animaciones, debe configurar el temporizador para que se deshabilite automáticamente. Para obtener más información, vea [animación controlada por temporizador](scenic-animation-api-overview.md).

## <a name="example-code"></a>Código de ejemplo

-   [Animación controlada por aplicaciones](#application-driven-animation)
-   [Animación controlada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animación

El siguiente código de ejemplo se toma de ManagerEventHandler. h de [la animación de Windows ejemplos de](application-driven-animation-sample.md) animación y [diseño de cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample). Define el controlador de eventos de administrador.


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



El siguiente código de ejemplo se toma de MainWindow. cpp de la animación de Windows de ejemplo Animation [orientada a la aplicación](application-driven-animation-sample.md). vea CMainWindow:: InitializeAnimation. En este ejemplo se crea una instancia del controlador de eventos Manager con el método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) y se pasa al administrador de animaciones mediante el método [**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .


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



Dado que el controlador de eventos de administrador conserva una referencia al objeto de ventana principal, el controlador de eventos de administrador debe borrarse (pasando **null** a [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) o el administrador de animaciones debe liberarse por completo antes de que se destruya la ventana principal.

El siguiente código de ejemplo se toma de MainWindow. cpp en la [animación de Windows de ejemplo animación controlada por la aplicación](application-driven-animation-sample.md); Vea el método CMainWindow:: OnPaint. Llama al método [**IUIAnimationManager:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) para recuperar la hora en las unidades requeridas por el método [**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .


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



El siguiente código de ejemplo se toma de MainWindow. cpp de la animación de Windows ejemplos de animación [orientada a la aplicación](application-driven-animation-sample.md) y el [diseño de cuadrículas](/windows/desktop/UIAnimation/grid-layout-sample). Vea el método CMainWindow:: OnPaint. Se supone que la aplicación está usando una API de gráficos que se sincroniza automáticamente con la frecuencia de actualización del monitor (como Direct2D con su configuración predeterminada), en cuyo caso una llamada a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) es suficiente para asegurarse de que se llamará de nuevo al código de dibujo cuando sea el momento de dibujar el fotograma siguiente. En lugar de llamar a **InvalidateRect** incondicionalmente, es mejor comprobar si todavía hay animaciones programadas mediante [**getStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


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



### <a name="timer-driven-animation"></a>Timer-Driven animación

El siguiente código de ejemplo se toma de TimerEventHandler. h de la animación de Windows de ejemplo Animation [controlada por temporizador](timer-driven-animation-sample.md). El código de ejemplo define el controlador de eventos Timer, que invalida el área cliente de la ventana para que se vuelva a dibujar después de cada actualización del estado de la animación.


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



El siguiente código de ejemplo se toma de MainWindow. cpp de la animación de Windows de ejemplo Animation [controlada por temporizador](timer-driven-animation-sample.md); vea CMainWindow:: InitializeAnimation. En este ejemplo se crea una instancia del controlador de eventos Timer con el método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) y se pasa al temporizador mediante el método [**IUIAnimationTimer:: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) . Dado que el controlador de eventos Timer conserva una referencia al objeto Window principal, el controlador de eventos Timer debe borrarse (pasando **null** a **SetTimerEventHandler**) o el temporizador completamente liberado antes de que se destruya la ventana principal.


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



El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplo de animación [controlada por temporizador](timer-driven-animation-sample.md); Vea el método CMainWindow:: InitializeAnimation. Llama al método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto de administrador de animaciones para obtener un puntero a [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)y, a continuación, conecta los objetos [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) y [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) estableciendo el administrador de animaciones como el controlador de actualización del temporizador mediante el método [**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) . Tenga en cuenta que no es necesario borrar explícitamente esta conexión; la conexión se borra de forma segura después de que la aplicación libera el administrador de animaciones y el temporizador de animación.


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



Si no se usa el **\_ \_ comportamiento de inactividad de animación \_ \_** de la interfaz de usuario, también es necesario habilitar el temporizador para iniciar la marcación.

## <a name="previous-step"></a>Paso anterior

Antes de comenzar este paso, debe haber completado este paso: [crear variables de animación](create-animation-variables.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el paso siguiente es [leer los valores de la variable de animación](updating---application-driven-animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer:: GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Información general sobre animaciones de Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 