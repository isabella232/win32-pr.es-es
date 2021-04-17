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
# <a name="hints-and-tips"></a><span data-ttu-id="fe071-103">Sugerencias y sugerencias</span><span class="sxs-lookup"><span data-stu-id="fe071-103">Hints and Tips</span></span>

<span data-ttu-id="fe071-104">A continuación se muestran sugerencias y sugerencias que se deben tener en cuenta al escribir una aplicación para TAPI 3:</span><span class="sxs-lookup"><span data-stu-id="fe071-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="fe071-105">La [**Coinicialización**](/windows/desktop/api/objbase/nf-objbase-coinitialize) com crea indirectamente ventanas; Esto es especialmente importante para los subprocesos de apartamento.</span><span class="sxs-lookup"><span data-stu-id="fe071-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="fe071-106">Si un subproceso crea cualquier ventana, debe procesar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="fe071-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="fe071-107">Si los subprocesos llaman a **CoInitialize**, ejecute un bombeo de mensajes para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="fe071-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="fe071-108">Por ejemplo, COM podría dejar de calcular las referencias correctamente o los métodos de las interfaces COM, como **IGlobalInterfaceTable** podrían bloquearse.</span><span class="sxs-lookup"><span data-stu-id="fe071-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="fe071-109">En los subprocesos de apartamento debe tener un bombeo de mensajes independientemente de si espera los objetos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="fe071-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="fe071-110">Esto es especialmente importante si tiene una aplicación de consola o escribe un objeto de servidor local o remoto de COM que sea de subprocesos de apartamento (donde no tiene una consola de o una GUI, pero el control solo se ejecuta en el sistema).</span><span class="sxs-lookup"><span data-stu-id="fe071-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="fe071-111">Al llamar a las funciones de espera y sincronización, como [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), etc.</span><span class="sxs-lookup"><span data-stu-id="fe071-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="fe071-112">En su lugar, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) y procese los mensajes, o bien use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), que detectará automáticamente el tipo de apartamento en el que se encuentra el subproceso (STA o MTA) y esperará en un bucle modal com (si STA) o se bloqueará en **WaitForMultipleObjects** (si es MTA).</span><span class="sxs-lookup"><span data-stu-id="fe071-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="fe071-113">**MsgWaitForMultipleObjects** y **CoWaitForMultipleHandles** también procesan los mensajes de Windows de acuerdo con las reglas com.</span><span class="sxs-lookup"><span data-stu-id="fe071-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="fe071-114">Por ejemplo, en lugar de:</span><span class="sxs-lookup"><span data-stu-id="fe071-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="fe071-115">Uso:</span><span class="sxs-lookup"><span data-stu-id="fe071-115">Use:</span></span>

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

2.  <span data-ttu-id="fe071-116">**ITTAPIEventNotification:: Event** es la función de evento apps llamada en un subproceso de devolución de llamada TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="fe071-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="fe071-117">Haga lo mínimo en la rutina de evento; en su lugar, use su propio subproceso siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="fe071-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="fe071-118">Tenga en cuenta que se proporciona el siguiente ejemplo de código, pero no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="fe071-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

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

3.  <span data-ttu-id="fe071-119">No manipule objetos COM después de llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="fe071-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="fe071-120">Los resultados son imprevisibles y perjudiciales para una aplicación correcta.</span><span class="sxs-lookup"><span data-stu-id="fe071-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="fe071-121">Algunos ejemplos en los que esto puede suceder son los subprocesos de trabajo y los destructores de C++ que se pueden ejecutar después de que una aplicación llame a **CoUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="fe071-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 
