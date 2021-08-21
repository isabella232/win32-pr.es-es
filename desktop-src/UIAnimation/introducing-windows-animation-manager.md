---
title: Actualizar el Administrador de animaciones y dibujar fotogramas
description: Cada vez que una aplicación programa un guión gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- objetos de administrador de animación Windows animación , actualización
- objetos de temporizador de animación Windows animation ,connecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd6c2c971783e13e00a45fe045be2624234f4165dc9fba1e50b11f88c69b68c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118847366"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>Actualizar el Administrador de animaciones y dibujar fotogramas

Cada vez que una aplicación programa un guión gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones. La hora actual también es necesaria al dirigir al administrador de animaciones para que actualice su estado y establezca todas las variables de animación en los valores interpolados adecuados.

## <a name="overview"></a>Información general

Hay dos configuraciones admitidas por Windows animación: animación controlada por la aplicación y animación controlada por temporizador.

Para usar la animación controlada por la aplicación en la aplicación, debe actualizar el administrador de animaciones antes de dibujar cada fotograma y usar un mecanismo adecuado para dibujar fotogramas con la frecuencia suficiente para la animación. Una aplicación que usa animación controlada por la aplicación puede usar cualquier mecanismo para determinar la hora actual, pero el objeto de temporizador de animación de Windows devuelve una hora precisa en las unidades aceptadas por el administrador de animaciones. Para evitar dibujos innecesarios cuando no se reproduce ninguna animación, también debe proporcionar un controlador de eventos de administrador para empezar a dibujar de nuevo cuando se programan animaciones y comprobar después de cada fotograma si se puede suspender el dibujo. Para obtener más información, vea [Animación controlada por la aplicación](scenic-animation-api-overview.md).

En la configuración controlada por la aplicación, una aplicación puede llamar al método [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) para comprobar que las animaciones están programadas actualmente y seguir dibujando fotogramas si lo están. Dado que el nuevo dibujo se detiene cuando no hay ninguna animación programada, es necesario reiniciarla la próxima vez que se programe una animación. Una aplicación puede registrar un controlador de eventos de administrador para recibir una notificación cuando el estado del administrador de animaciones cambie de inactivo (no hay animaciones programadas actualmente) a ocupado.

Para usar la animación controlada por temporizador en la aplicación, debe conectar el administrador de animaciones a un temporizador de animación y proporcionar un controlador de eventos de temporizador. Cuando el administrador de animación está conectado a un temporizador, el temporizador puede decir al administrador cuándo debe actualizarse el estado de animación a medida que avanza el tiempo. La aplicación debe dibujar un marco para cada paso del temporizador. A su vez, el administrador de animaciones puede avisarle al temporizador cuando se reproducen animaciones, por lo que el temporizador puede apagarse durante períodos de inactividad cuando no es necesario volver a dibujar. Para evitar dibujos innecesarios cuando no se reproduce ninguna animación, debe configurar el temporizador para deshabilitarse automáticamente. Para obtener más información, vea [Animación controlada por temporizador.](scenic-animation-api-overview.md)

## <a name="example-code"></a>Código de ejemplo

-   [Animación controlada por la aplicación](#application-driven-animation)
-   [Animación controlada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animación

El código de ejemplo siguiente se toma de ManagerEventHandler.h de los ejemplos de animación Windows aplicación y [diseño](application-driven-animation-sample.md) [de cuadrícula.](/windows/desktop/UIAnimation/grid-layout-sample) Define el controlador de eventos del administrador.


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



El código de ejemplo siguiente se toma de MainWindow.cpp de la Windows animación controlada por [la aplicación](application-driven-animation-sample.md)de ejemplo ; vea CMainWindow::InitializeAnimation. En este ejemplo se crea una instancia del controlador de eventos manager mediante el método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) y se pasa al administrador de animaciones mediante el método [**IUIAnimationManager::SetManagerEventHandler.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)


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



Dado que el controlador de eventos de administrador conserva una referencia al objeto de ventana principal, se debe borrar el controlador de eventos del administrador (pasando **NULL** a [**SetManagerEventHandler)**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)o el administrador de animaciones debe liberarse por completo antes de que se destruya la ventana principal.

El código de ejemplo siguiente se toma de MainWindow.cpp en el ejemplo Windows animación controlada por [la aplicación](application-driven-animation-sample.md); vea el método CMainWindow::OnPaint. Llama al [**método IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) para recuperar la hora en las unidades requeridas por el método [**IUIAnimationManager::Update.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)


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



El código de ejemplo siguiente se toma de MainWindow.cpp de los ejemplos Windows Animación controlada por la aplicación [y](application-driven-animation-sample.md) [Diseño de cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample); vea el método CMainWindow::OnPaint. Se supone que la aplicación usa una API de gráficos que se sincroniza automáticamente con la frecuencia de actualización del monitor (por ejemplo, Direct2D con su configuración predeterminada), en cuyo caso una llamada a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) es suficiente para asegurarse de que se volverá a llamar al código de dibujo cuando llegue el momento de dibujar el fotograma siguiente. En lugar de **llamar a InvalidateRect** incondicionalmente, es mejor comprobar si todavía hay animaciones programadas mediante [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


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

El código de ejemplo siguiente se toma de TimerEventHandler.h de la animación controlada por temporizador Windows [ejemplo de animación](timer-driven-animation-sample.md). El código de ejemplo define el controlador de eventos de temporizador, que invalida el área de cliente de la ventana para provocar un repintado después de cada actualización del estado de animación.


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



El código de ejemplo siguiente se toma de MainWindow.cpp de la animación controlada por temporizador de Windows [ejemplo de animación](timer-driven-animation-sample.md); vea CMainWindow::InitializeAnimation. En este ejemplo se crea una instancia del controlador de eventos timer mediante el [**método CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) y se pasa al temporizador mediante el método [**IUIAnimationTimer::SetTimerEventHandler.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) Dado que el controlador de eventos de temporizador conserva una referencia al objeto de ventana principal, se debe borrar el controlador de eventos del temporizador (pasando **NULL** a **SetTimerEventHandler)** o el temporizador liberado completamente antes de que se destruya la ventana principal.


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



El código de ejemplo siguiente se toma de MainWindow.cpp en el ejemplo Windows animación controlada por [temporizador](timer-driven-animation-sample.md); vea el método CMainWindow::InitializeAnimation. Llama al método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto de administrador de animación para obtener un puntero a [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)y, a continuación, conecta los objetos [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) y [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) estableciendo el administrador de animaciones como controlador de actualizaciones del temporizador mediante el método [**IUIAnimationTimer::SetTimerUpdateHandler.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) Tenga en cuenta que no es necesario borrar explícitamente esta conexión; La conexión se borra de forma segura después de que la aplicación libere el administrador de animaciones y el temporizador de animación.


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



Si **no se usa UI ANIMATION IDLE BEHAVIOR \_ \_ \_ \_ DISABLE,** también es necesario habilitar el temporizador para iniciar el tic.

## <a name="previous-step"></a>Paso anterior

Antes de iniciar este paso, debe haber completado este paso: Crear [variables de animación](create-animation-variables.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el siguiente paso es: [Leer los valores de variable de animación](updating---application-driven-animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Windows Información general sobre animaciones](scenic-animation-api-overview.md)
</dt> </dl>

 

 