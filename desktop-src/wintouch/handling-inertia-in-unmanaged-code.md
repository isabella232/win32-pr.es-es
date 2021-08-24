---
title: Control de la inercia en código no administrado
description: En esta sección se explica cómo usar la interfaz IInertiaProcessor para controlar la inercia en código no administrado.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Windows Touch,inertia
- Windows Táctil, procesador de manipulación
- inercia, código no administrado
- inertia,IInertiaProcessor (interfaz)
- inercia, procesador de manipulación
- procesador de manipulación, inercia
- Interfaz IInertiaProcessor, código no administrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e112605b1f998b850c3a04a045166b376fc3a12d98615b9c2af72e756a1c1b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346505"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Control de la inercia en código no administrado

En esta sección se explica cómo usar la [**interfaz IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para controlar la inercia en código no administrado.

## <a name="overview"></a>Información general

Para usar la inercia en código no administrado, debe implementar receptores de eventos tanto para el procesador de manipulación como para el procesador de inercia. Empiece agregando compatibilidad con la manipulación a la aplicación como se describe en la sección [Adding Manipulation Support to Unmanaged Code](adding-manipulation-support-in-unmanaged-code.md). Tenga en cuenta que la compatibilidad con la manipulación requiere el uso de mensajes táctiles en lugar de mensajes de gestos para enviar datos de eventos al procesador de manipulación. Después de que la manipulación funcione, también debe implementar un segundo receptor de eventos para los eventos que la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) va a generar o deberá modificar el receptor de eventos existente para dar cabida a los eventos generados por las interfaces **IInertiaProcessor** e [**IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) Para los fines de este ejemplo, es más fácil empezar desde el receptor de eventos creado para la sección Adding Manipulation Support to Unmanaged Code (Agregar compatibilidad con la manipulación al código no administrado) y agregar un segundo constructor que funcione con el procesador de inercia en lugar del procesador de manipulación. De este modo, la implementación del receptor de eventos puede funcionar para el procesador de manipulación o el procesador de inercia. Además de agregar un segundo constructor, el receptor de eventos tendrá una variable que indica si realizará las operaciones en función de la entrada de inercia en lugar de la entrada de manipulación.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Agregar compatibilidad con inercia a un receptor de eventos de procesador de manipulación

El código siguiente muestra el nuevo constructor receptor de eventos, nuevas variables miembro para una [**interfaz IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) y una marca que indica si el receptor se está extrayendo para la inercia.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



Una vez que el encabezado de clase tiene los nuevos constructores y una marca que indica si va a extrapolar, puede implementar el receptor de eventos para que tenga bloques de control independientes para los eventos [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) y los eventos [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) El constructor que acepta un **IManipulationProcessor** y un **IInertiaProcessor** debe establecer la marca **fExtrapolating** en false, lo que indica que se trata de un controlador de eventos **IManipulationProcessor.** El código siguiente muestra cómo se podría implementar el constructor para un receptor de eventos que usa **IManipulationProcessor.**


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}
```



El código siguiente muestra cómo se podría implementar el constructor para un receptor de eventos que usa [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Este constructor establece la marca **fExtrapolating** en true, lo que indica que esta instancia de la clase receptora de eventos realizará la extrapolación y realizará las operaciones de movimiento realizadas anteriormente por los eventos del procesador de manipulación.


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }
    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}   
```



> [!Note]  
> La implementación de la clase de receptor de eventos del receptor de eventos del procesador de manipulación se reutiliza como receptor de eventos para el procesador de inercia.

 

Ahora, cuando se construye esta clase, **CManipulationEventSink,** se puede construir como receptor de eventos para un procesador de manipulación o como receptor de eventos para un procesador de inercia. Cuando se construye como receptor de eventos de procesador de inercia, tendrá la marca **fExtrapolating** establecida en true, lo que indica que los eventos de manipulación se deben extrapolar.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) se genera mediante las interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)

 

Cuando se inicia la manipulación, se establecen las propiedades de la interfaz [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) El código siguiente muestra cómo se controla el evento iniciado.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



En este ejemplo, se usan deltas de manipulación para mover la ventana. El código siguiente muestra cómo se controla el evento delta.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
        
    RECT rect;
            
    GetWindowRect(m_hWnd, &rect);
        
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



En este ejemplo, la manipulación completó eventos que inician o detienen un temporizador que llamará a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) en la [**interfaz IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) El código siguiente muestra cómo se controla el evento de manipulación completado.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



El código siguiente muestra cómo podría interpretar los mensajes **WM \_ TIMER** en **WndProc para** realizar llamadas a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) en la [**interfaz IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>Inicializar el procesador de inercia y el procesador de manipulación e inicializar los receptores de eventos

Después de modificar el receptor de eventos para admitir [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) y [**IInertiaProcessor,**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)está listo para inicializar los receptores de eventos y configurarlos para que se ejecuten desde la aplicación. El código siguiente muestra cómo se asignan los punteros de interfaz.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



En el ejemplo de código siguiente se muestra cómo crear instancias de las interfaces.


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



En el ejemplo de código siguiente se muestra cómo construir los receptores de eventos dados los punteros de interfaz y registrar la ventana para la entrada táctil.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inercia](getting-started-with-inertia.md)
</dt> </dl>

 

 




