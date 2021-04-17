---
description: A continuación se indican sugerencias y sugerencias que se deben tener en cuenta al escribir una aplicación para TAPI 3.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Sugerencias y sugerencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689712"
---
# <a name="hints-and-tips"></a>Sugerencias y sugerencias

A continuación se muestran sugerencias y sugerencias que se deben tener en cuenta al escribir una aplicación para TAPI 3:

1.  La [**Coinicialización**](/windows/desktop/api/objbase/nf-objbase-coinitialize) com crea indirectamente ventanas; Esto es especialmente importante para los subprocesos de apartamento. Si un subproceso crea cualquier ventana, debe procesar los mensajes. Si los subprocesos llaman a **CoInitialize**, ejecute un bombeo de mensajes para evitar problemas. Por ejemplo, COM podría dejar de calcular las referencias correctamente o los métodos de las interfaces COM, como **IGlobalInterfaceTable** podrían bloquearse.

    En los subprocesos de apartamento debe tener un bombeo de mensajes independientemente de si espera los objetos de sincronización. Esto es especialmente importante si tiene una aplicación de consola o escribe un objeto de servidor local o remoto de COM que sea de subprocesos de apartamento (donde no tiene una consola de o una GUI, pero el control solo se ejecuta en el sistema).

    > [!Caution]  
    > Al llamar a las funciones de espera y sincronización, como [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), etc. En su lugar, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) y procese los mensajes, o bien use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), que detectará automáticamente el tipo de apartamento en el que se encuentra el subproceso (STA o MTA) y esperará en un bucle modal com (si STA) o se bloqueará en **WaitForMultipleObjects** (si es MTA). **MsgWaitForMultipleObjects** y **CoWaitForMultipleHandles** también procesan los mensajes de Windows de acuerdo con las reglas com.

     

    Por ejemplo, en lugar de:

    `Sleep (5000);`

    Uso:

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  **ITTAPIEventNotification:: Event** es la función de evento apps llamada en un subproceso de devolución de llamada TAPI 3.

    Haga lo mínimo en la rutina de evento; en su lugar, use su propio subproceso siempre que sea posible.

    Tenga en cuenta que se proporciona el siguiente ejemplo de código, pero no es un requisito.

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  No manipule objetos COM después de llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Los resultados son imprevisibles y perjudiciales para una aplicación correcta. Algunos ejemplos en los que esto puede suceder son los subprocesos de trabajo y los destructores de C++ que se pueden ejecutar después de que una aplicación llame a **CoUninitialize**.

 

 
