---
title: Ejemplo de manipulación e inercia
description: En el ejemplo de manipulación e inercia se muestra cómo agregar compatibilidad con Windows Touch a aplicaciones nativas basadas en Windows que usan la API Touch de Windows.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch, manipulaciones
- Windows Touch, inercia
- Ejemplo de toque, manipulación e inercia de Windows
- Ejemplo de manipulación e inercia
- Windows Touch, _IManipulationEventSink interfaz
- Windows Touch, interfaz IManipulationProcessor
- Windows Touch, interfaz IInertiaProcessor
- manipulaciones, código de ejemplo
- manipulaciones, ejemplos de código
- manipulaciones, _IManipulationEventSink interfaz
- manipulaciones, interfaz IManipulationProcessor
- inercia, código de ejemplo
- inercia, ejemplos de código
- inercia, interfaz IInertiaProcessor
- Interfaz _IManipulationEventSink
- IManipulationProcessor (interfaz), ejemplos de código
- Interfaz IManipulationProcessor, código de ejemplo
- IInertiaProcessor (interfaz), ejemplos de código
- Interfaz IInertiaProcessor, código de ejemplo
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: a17b634fbe79d72e79fc5c9e03ef64a30cb46411
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555875"
---
# <a name="manipulation-and-inertia-sample"></a><span data-ttu-id="3d2a6-124">Ejemplo de manipulación e inercia</span><span class="sxs-lookup"><span data-stu-id="3d2a6-124">Manipulation and Inertia Sample</span></span>

<span data-ttu-id="3d2a6-125">En el ejemplo de manipulación e inercia se muestra cómo agregar compatibilidad con Windows Touch a aplicaciones nativas basadas en Windows que usan la API Touch de Windows.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-125">The Manipulation and Inertia sample shows how to add Windows Touch support to native Windows-based applications that use the Windows Touch API.</span></span> <span data-ttu-id="3d2a6-126">En el ejemplo se implementan las características básicas de la API para habilitar la traducción, la rotación y el escalado de objetos y la aplicación de propiedades de inercia a ellos.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-126">The sample implements the basic features of the API to enable translation, rotation, and scaling for objects and applying inertia properties to them.</span></span> <span data-ttu-id="3d2a6-127">En el ejemplo también se muestra cómo ofrecer compatibilidad básica con el mouse de las aplicaciones táctiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-127">The sample also shows how to give your Windows Touch applications basic mouse support.</span></span> <span data-ttu-id="3d2a6-128">En la imagen siguiente se muestra el aspecto del ejemplo cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-128">The following image shows how the sample looks when it runs.</span></span>

![captura de pantalla que muestra dos cuadros con degradados en el ejemplo de manipulación e inercia](images/manip-inertia-sample.png)

<span data-ttu-id="3d2a6-130">Los cuadros con degradados se pueden manipular de forma independiente por un usuario cuando ejecutan la aplicación desde un equipo que admita Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-130">The boxes with gradients can be manipulated independently by a user when they run the application from a computer that supports Windows Touch.</span></span>

## <a name="register-the-touch-window"></a><span data-ttu-id="3d2a6-131">Registrar la ventana táctil</span><span class="sxs-lookup"><span data-stu-id="3d2a6-131">Register the Touch Window</span></span>

<span data-ttu-id="3d2a6-132">Para poder recibir entradas táctiles, primero debe notificar al sistema que la aplicación es una aplicación táctil de Windows mediante una llamada a la siguiente función:</span><span class="sxs-lookup"><span data-stu-id="3d2a6-132">Before you can receive touch input, you first must notify the system that your application is a Windows Touch application by calling the following function:</span></span>

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a><span data-ttu-id="3d2a6-133">Implementar la interfaz _IManipulationEventSink</span><span class="sxs-lookup"><span data-stu-id="3d2a6-133">Implement the _IManipulationEventSink Interface</span></span>

<span data-ttu-id="3d2a6-134">El receptor de eventos [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) contiene tres funciones: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)y [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted).</span><span class="sxs-lookup"><span data-stu-id="3d2a6-134">The [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink contains three functions: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted).</span></span> <span data-ttu-id="3d2a6-135">Estas funciones de devolución de llamada las utilizan la interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) y la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para devolver los valores calculados por los procesadores después de invocar las funciones [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)y [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) .</span><span class="sxs-lookup"><span data-stu-id="3d2a6-135">These callback functions are used by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface and [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for returning the values calculated by the processors after they invoke the [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime), and [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) functions.</span></span> <span data-ttu-id="3d2a6-136">En el ejemplo de código siguiente se muestra un ejemplo de implementación de una interfaz **_IManipulationEvents** .</span><span class="sxs-lookup"><span data-stu-id="3d2a6-136">The following code example shows an example implementation of a **_IManipulationEvents** interface.</span></span>

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

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a><span data-ttu-id="3d2a6-137">Creación de objetos COM y configuración de las interfaces IManipulationProcessor y IInertiaProcessor</span><span class="sxs-lookup"><span data-stu-id="3d2a6-137">Create COM Objects and Set up the IManipulationProcessor and IInertiaProcessor Interfaces</span></span>

<span data-ttu-id="3d2a6-138">La API proporciona una implementación de las interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) y [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="3d2a6-138">The API provides an implementation of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) and [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span> <span data-ttu-id="3d2a6-139">Debe crear una instancia de y hacer referencia a los objetos COM del receptor de eventos [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que se implementó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-139">You should create an instance of and reference the COM objects from the [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink that was implemented earlier.</span></span>

## <a name="handle-wm_touch-messages"></a><span data-ttu-id="3d2a6-140">Controlar mensajes de WM_TOUCH</span><span class="sxs-lookup"><span data-stu-id="3d2a6-140">Handle WM_TOUCH Messages</span></span>

<span data-ttu-id="3d2a6-141">Los datos de entrada deben extraerse de los mensajes [**WM_TOUCH**](wm-touchdown.md) y, posteriormente, se deben procesar para alimentar el procesador de manipulación correcto.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-141">The input data must be extracted from the [**WM_TOUCH**](wm-touchdown.md) messages and then later must be processed to feed the correct manipulation processor.</span></span>

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
> <span data-ttu-id="3d2a6-142">Para poder usar la función [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , debe tener compatibilidad con PPP alta en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-142">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="3d2a6-143">Para obtener más información acerca de la compatibilidad con altas PPP, visite la sección de [PPP alta]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-143">For more information about supporting high DPI, visit the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a><span data-ttu-id="3d2a6-144">Pasar estructuras TOUCHINPUT al procesador adecuado</span><span class="sxs-lookup"><span data-stu-id="3d2a6-144">Pass TOUCHINPUT Structures to the Appropriate Processor</span></span>

<span data-ttu-id="3d2a6-145">Una vez que los datos se extraen de los mensajes de [**WM_TOUCH**](wm-touchdown.md) mediante la función [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) , inserte los datos en el procesador de manipulación mediante la invocación de las funciones [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)o [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) , en función del conjunto de **dwFlag** de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) .</span><span class="sxs-lookup"><span data-stu-id="3d2a6-145">After the data is extracted from the [**WM_TOUCH**](wm-touchdown.md) messages by using the [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) function, feed the data into the manipulation processor by invoking [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime), or [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) functions, depending on the **dwFlag** set in the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure.</span></span>

> [!Note]  
> <span data-ttu-id="3d2a6-146">Cuando se admiten varias manipulaciones, se debe crear un nuevo procesador de manipulación si se debe usar el **dwID** definido en la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) para enviar los datos al objeto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) correcto.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-146">When supporting multiple manipulations, a new manipulation processor must be created if the **dwID** defined in the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure must be used to send the data to the correct [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) object.</span></span>

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

## <a name="set-up-inertia-within-manipulationcompleted"></a><span data-ttu-id="3d2a6-147">Configuración de la inercia dentro de ManipulationCompleted</span><span class="sxs-lookup"><span data-stu-id="3d2a6-147">Set up Inertia within ManipulationCompleted</span></span>

<span data-ttu-id="3d2a6-148">Después de invocar el método [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) , el objeto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) debe establecer los valores del objeto [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) vinculado a **IManipulationProcessor** para invocar la inercia.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-148">After the [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) method is invoked, the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) object must set the values for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) object linked to the **IManipulationProcessor** to invoke inertia.</span></span> <span data-ttu-id="3d2a6-149">En el ejemplo de código siguiente se muestra cómo configurar el objeto **IInertiaProcessor** desde el método **IManipulationProcessor** **ManipulationCompleted**.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-149">The following code example shows how to set up the **IInertiaProcessor** object from the **IManipulationProcessor** method **ManipulationCompleted**.</span></span>

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

## <a name="clean-up-your-com-objects"></a><span data-ttu-id="3d2a6-150">Limpie los objetos COM</span><span class="sxs-lookup"><span data-stu-id="3d2a6-150">Clean up your COM Objects</span></span>

<span data-ttu-id="3d2a6-151">Cuando se cierre la aplicación, debe limpiar los objetos COM.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-151">When your application closes, you must clean up your COM objects.</span></span> <span data-ttu-id="3d2a6-152">En el código siguiente se muestra cómo se pueden liberar los recursos que se asignaron en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3d2a6-152">The following code shows how you can free the resources that were allocated in the sample.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3d2a6-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d2a6-153">Related topics</span></span>

<span data-ttu-id="3d2a6-154">[Aplicación de manipulación multitáctil](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [ejemplo de manipulación e inercia](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="3d2a6-154">[Multi-touch Manipulation Application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation and Inertia Sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>