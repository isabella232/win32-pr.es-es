---
title: Agregar compatibilidad de manipulación en código no administrado
description: En esta sección se explica cómo agregar compatibilidad de manipulación a código no administrado implementando un receptor de eventos para la \_ interfaz IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Touch, manipulaciones
- Windows Touch, _IManipulationEvents interfaz
- Windows Touch, interfaz IManipulationProcessor
- manipulaciones, agregar compatibilidad en código no administrado
- manipulaciones, compatibilidad con código no administrado
- manipulaciones, compatibilidad en código no administrado
- manipulaciones, _IManipulationEvents interfaz
- manipulaciones, interfaz IManipulationProcessor
- _IManipulationEvents interfaz, compatibilidad de manipulación en código no administrado
- Interfaz IManipulationProcessor, compatibilidad de manipulación en código no administrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149488"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Agregar compatibilidad de manipulación en código no administrado

En esta sección se explica cómo agregar compatibilidad de manipulación a código no administrado implementando un receptor de eventos para la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

En la imagen siguiente se describe la arquitectura de manipulación.

![Ilustración en la que se muestran los mensajes táctiles de Windows que se pasan al procesador de manipulación de un objeto, que controla los eventos con la \- interfaz imanipulationevents](images/manipulation-arch.png)

Los datos táctiles que se reciben de los mensajes [**\_ Touch de WM**](wm-touchdown.md) se pasan a [**IMANIPULATIONPROCESSOR**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) junto con el identificador de contacto del mensaje Touch. En función de la secuencia de mensajes, la interfaz **IManipulationProcessor** calculará el tipo de transformación que se va a realizar y los valores asociados a esta transformación. A continuación, **IManipulationProcessor** generará [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que se controla mediante un receptor de eventos. Después, el receptor de eventos puede utilizar estos valores para realizar operaciones personalizadas en el objeto que se va a transformar.

Para agregar compatibilidad de manipulación a la aplicación, debe seguir estos pasos:

1.  Implemente un receptor de eventos para la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .
2.  Cree una instancia de una interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .
3.  Cree una instancia del receptor de eventos y configure eventos táctiles.
4.  Envíe datos de eventos táctiles al procesador de manipulación.

En esta sección se explican los pasos que debe seguir para agregar compatibilidad de manipulación a la aplicación. En cada paso se proporciona código para comenzar.

> [!Note]  
> No se pueden usar manipulaciones y gestos al mismo tiempo porque los mensajes de gestos y táctiles son mutuamente excluyentes.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementación de un receptor de eventos para la \_ interfaz IManipualtionEvents

Antes de poder crear una instancia del receptor de eventos, debe crear una clase que implemente la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) para el evento. Este es el receptor de eventos. El receptor de eventos controla los eventos generados por la interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . En el código siguiente se muestra un encabezado de ejemplo para una clase que hereda la interfaz **\_ IManipulationEvents** .

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
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
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

Dado el encabezado, debe crear una implementación de la interfaz de eventos para que la clase realice las acciones que desea que realice el procesador de manipulación. El código siguiente es una plantilla que implementa la funcionalidad mínima de un receptor de eventos para la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
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

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

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
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

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

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

Preste especial atención a las implementaciones de los métodos [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)y [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) en la clase. Estos son los métodos más probables en la interfaz que requerirán que realice operaciones basadas en la información de manipulación que se pasa en el evento. Tenga en cuenta también que el segundo parámetro del constructor es el objeto que se usa en las manipulaciones de eventos. En el código que se usa para generar el ejemplo, el hWnd de la aplicación se envía al constructor para que se pueda cambiar su posición y cambiar su tamaño.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Crear una instancia de una interfaz IManipulationProcessor

En el código donde usará manipulaciones, debe crear una instancia de una interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . En primer lugar, debe agregar compatibilidad con la clase manipulaciones. En el código siguiente se muestra cómo puede hacer esto en la clase.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Una vez que tenga la variable para el procesador de manipulación y haya incluido los encabezados para las manipulaciones, tendrá que crear una instancia de la interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Se trata de un objeto COM. Por lo tanto, debe llamar a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)y, a continuación, crear una instancia de la referencia a **IManipulationProcessor**. En el código siguiente se muestra cómo se puede crear una instancia de esta interfaz.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Creación de una instancia del receptor de eventos y configuración de eventos táctiles

Incluya la definición de la clase de receptor de eventos en el código y, a continuación, agregue una variable para la clase de receptor de eventos de manipulación. En el ejemplo de código siguiente se incluye el encabezado para la implementación de la clase y se establece una variable global para almacenar el receptor de eventos.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Una vez que tenga la variable y haya incluido su definición para la nueva clase de receptor de eventos, puede construir la clase mediante el procesador de manipulación que ha configurado en el paso anterior. En el código siguiente se muestra cómo se crearía una instancia de esta clase a partir de **OnInitDialog**.

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> La forma de crear una instancia del receptor de eventos depende de lo que esté haciendo con los datos de manipulación. En la mayoría de los casos, creará un receptor de eventos de procesador de manipulación que no tiene el mismo constructor que este ejemplo.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Envío de datos de eventos táctiles al procesador de manipulación

Ahora que tiene el procesador de manipulación y el receptor de eventos configurados, debe alimentar los datos táctiles en el procesador de manipulación para desencadenar eventos de manipulación.

> [!Note]  
> Este es el mismo procedimiento que se describe en [Introducción con mensajes táctiles de Windows](getting-started-with-multi-touch-messages.md).

En primer lugar, creará código para descodificar los mensajes [**\_ Touch de WM**](wm-touchdown.md) y enviarlos a la interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) para generar eventos. En el código siguiente se muestra una implementación de ejemplo a la que se llama desde el método **WndProc** y se devuelve un **LRESULT** para mensajería.

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

Ahora que tiene un método de utilidad para descodificar el mensaje de [**\_ pantalla táctil de WM**](wm-touchdown.md) , debe pasar los mensajes **\_ Touch de WM** a la función de utilidad desde el método **WndProc** . En el código siguiente se muestra cómo puede hacerlo.

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

Los métodos personalizados que ha implementado en el receptor de eventos deberían funcionar ahora. En este ejemplo, al tocar la ventana se moverá.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>


 