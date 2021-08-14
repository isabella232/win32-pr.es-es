---
description: A continuación se incluyen sugerencias y sugerencias que se deben tener en cuenta al escribir una aplicación para TAPI 3.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Sugerencias y Sugerencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d51e8c7e3f8c6e4a9e38b27fa5cfe4c10e45d37cfa67af095d573eea319614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762943"
---
# <a name="hints-and-tips"></a>Sugerencias y Sugerencias

A continuación se incluyen sugerencias y sugerencias que se deben tener en cuenta al escribir una aplicación para TAPI 3:

1.  COM [**CoInitialize crea**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ventanas indirectamente; esto es especialmente importante para el subprocesamiento de apartamento. Si un subproceso crea ventanas, debe procesar los mensajes. Si los subprocesos llaman a **CoInitialize,** ejecute un bombeo de mensajes para evitar problemas. Por ejemplo, COM podría dejar de obtener la configuración de cálculo de la base de datos correctamente o los métodos de las interfaces COM, como **IGlobalInterfaceTable,** podrían no funcionar.

    En el subprocesamiento de apartamento debe tener un bombeo de mensajes independientemente de si espera objetos de sincronización. Esto es especialmente importante si tiene una aplicación de consola o escribe un objeto de servidor local o remoto COM que está en un subproceso de apartamento (donde no tiene una consola o una GUI, pero el control simplemente "se ejecuta" en el sistema).

    > [!Caution]  
    > Al llamar a las funciones de espera y sincronización, como [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)y así sucesivamente. En su lugar, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) y procese los mensajes, o [**use CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), que detectará automáticamente en qué tipo de apartamento se encuentra el subproceso (STA o MTA) y esperará en un bucle modal COM (si es STA) o bloqueará **en WaitForMultipleObjects** (si MTA). **MsgWaitForMultipleObjects** y **CoWaitForMultipleHandles** también procesan mensajes de Windows según las reglas COM.

     

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

2.  **ITTAPIEventNotification::Event** es la función event de aplicaciones a la que se llama en un subproceso de devolución de llamada TAPI 3.

    Realice el mínimo en la rutina Event; en su lugar, use su propio subproceso siempre que sea posible.

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

3.  No manipule objetos COM después de llamar [**a CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Los resultados son impredecibles y perjudiciales para una aplicación en buen estado. Algunos ejemplos en los que esto puede ocurrir son subprocesos de trabajo y destructores de C++ que se pueden ejecutar después de que una aplicación llame a **CoUninitialize**.

 

 
