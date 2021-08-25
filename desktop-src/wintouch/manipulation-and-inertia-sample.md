---
title: Ejemplo de manipulación e inercia
description: El ejemplo de manipulación e inercia muestra cómo agregar compatibilidad con Windows Touch a aplicaciones nativas basadas en Windows que usan Windows Touch API.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Touch,ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch,manipulations
- Windows Touch,inertia
- Windows Touch,Manipulation and Inertia sample
- Ejemplo de manipulación e inercia
- Windows Touch,_IManipulationEventSink interfaz
- Windows Interfaz Touch,IManipulationProcessor
- Windows Interfaz Touch,IInertiaProcessor
- manipulaciones, código de ejemplo
- manipulaciones, ejemplos de código
- manipulaciones, _IManipulationEventSink interfaz
- manipulations,IManipulationProcessor (interfaz)
- inercia, código de ejemplo
- inercia, ejemplos de código
- inertia,IInertiaProcessor (interfaz)
- _IManipulationEventSink interfaz
- Interfaz IManipulationProcessor, ejemplos de código
- Interfaz IManipulationProcessor, código de ejemplo
- Interfaz IInertiaProcessor, ejemplos de código
- Interfaz IInertiaProcessor, código de ejemplo
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8b6471362d30b6efc9dfa0c4f07df70f014c8cb72866c92bbb04c9eb33463410
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840604"
---
# <a name="manipulation-and-inertia-sample"></a>Ejemplo de manipulación e inercia

El ejemplo de manipulación e inercia muestra cómo agregar compatibilidad con Windows Touch a aplicaciones nativas basadas en Windows que usan Windows Touch API. El ejemplo implementa las características básicas de la API para habilitar la traducción, rotación y escalado de objetos y aplicarles propiedades de inercia. En el ejemplo también se muestra cómo proporcionar a las aplicaciones Windows Touch compatibilidad básica con el mouse. En la imagen siguiente se muestra el aspecto del ejemplo cuando se ejecuta.

![captura de pantalla que muestra dos cuadros con degradados en la muestra de manipulación e inercia](images/manip-inertia-sample.png)

Un usuario puede manipular los cuadros con degradados de forma independiente cuando ejecutan la aplicación desde un equipo que admite Windows Touch.

## <a name="register-the-touch-window"></a>Registro de la ventana táctil

Para poder recibir la entrada táctil, primero debe notificar al sistema que la aplicación es una aplicación Windows Touch mediante una llamada a la función siguiente:

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>Implementación de la _IManipulationEventSink interfaz

El [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) de eventos contiene tres funciones: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)y [**ManipulationCompleted.**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) La interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) y la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) usan estas funciones de devolución de llamada para devolver los valores calculados por los procesadores después de invocar las funciones [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime) [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)y [**ProcessMoveWithTime.**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) En el ejemplo de código siguiente se muestra una implementación de ejemplo de **_IManipulationEvents** interfaz.

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>Crear objetos COM y configurar las interfaces IManipulationProcessor e IInertiaProcessor

La API proporciona una implementación de las interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) [**e IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Debe crear una instancia de y hacer referencia a los objetos COM desde el receptor de eventos [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que se implementó anteriormente.

## <a name="handle-wm_touch-messages"></a>Control de WM_TOUCH mensajes

Los datos de entrada se deben extraer de los WM_TOUCH y, [**a**](wm-touchdown.md) continuación, se deben procesar para alimentar el procesador de manipulación correcto.

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> Para usar la función [**ScreenToClient,**](/windows/desktop/api/winuser/nf-winuser-screentoclient) debe tener compatibilidad con valores altos de PPP en la aplicación. Para obtener más información sobre la compatibilidad con valores altos de PPP, visite la [sección Valores altos de PPP]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>Pasar estructuras TOUCHINPUT al procesador adecuado

Después de extraer los datos de los mensajes [**de WM_TOUCH**](wm-touchdown.md) mediante la función [**GetTouchInputInfo,**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) invoque los datos en el procesador de manipulación invocando las funciones [**ProcessUpWithTime,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime) [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)o [**ProcessMoveWithTime,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) en función del **conjunto dwFlag** en la [**estructura TOUCHINPUT.**](/windows/win32/api/winuser/ns-winuser-touchinput)

> [!Note]  
> Al admitir varias manipulaciones, se debe crear un nuevo procesador de manipulación si el **dwID** definido en la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) debe usarse para enviar los datos al objeto [**IManipulationProcessor correcto.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>Configuración de la inercia en ManipulationCompleted

Después de invocar el método [**ManipulationCompleted,**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) el objeto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) debe establecer los valores del objeto [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) vinculado a **IManipulationProcessor** para invocar la inercia. En el ejemplo de código siguiente se muestra cómo configurar el objeto **IInertiaProcessor** desde el método **IManipulationProcessor** **ManipulationCompleted**.

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>Limpieza de los objetos COM

Cuando se cierre la aplicación, debe limpiar los objetos COM. El código siguiente muestra cómo puede liberar los recursos asignados en el ejemplo.

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>Temas relacionados

[Aplicación de manipulación multi táctil,](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp) [ejemplo de manipulación](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp)e [inercia, Windows touch samples](windows-touch-samples.md)