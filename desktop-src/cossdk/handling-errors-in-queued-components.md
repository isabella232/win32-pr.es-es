---
description: En ocasiones, se produce una situación en la que un mensaje no se puede entregar correctamente a su destino previsto, normalmente debido a un problema con el sistema o la configuración.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Control de errores en componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539057"
---
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="222bb-103">Control de errores en componentes en cola</span><span class="sxs-lookup"><span data-stu-id="222bb-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="222bb-104">En ocasiones, se produce una situación en la que un mensaje no se puede entregar correctamente a su destino previsto, normalmente debido a un problema con el sistema o la configuración.</span><span class="sxs-lookup"><span data-stu-id="222bb-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="222bb-105">Por ejemplo, puede que el mensaje se dirija a una cola que no existe o a que la cola de destino no esté en un estado para recibir.</span><span class="sxs-lookup"><span data-stu-id="222bb-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="222bb-106">El Movedor de mensajes es una herramienta que mueve todos los mensajes de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) con errores de una cola a otra para que se puedan Reintentar.</span><span class="sxs-lookup"><span data-stu-id="222bb-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="222bb-107">La utilidad del Movedor de mensajes es un objeto de automatización que se puede invocar con un VBScript.</span><span class="sxs-lookup"><span data-stu-id="222bb-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="222bb-108">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="222bb-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="222bb-109">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="222bb-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="222bb-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="222bb-110">Visual Basic</span></span>

<span data-ttu-id="222bb-111">En el código de ejemplo siguiente se muestra cómo crear un objeto MessageMover, cómo establecer las propiedades necesarias y cómo iniciar la transferencia.</span><span class="sxs-lookup"><span data-stu-id="222bb-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="222bb-112">Para usarlo desde Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="222bb-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="222bb-113">Para usar el objeto MessageMover, debe tener Message Queue Server instalado en el equipo y la aplicación especificada por AppName debe tener habilitada la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="222bb-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="222bb-114">Para obtener información acerca de cómo instalar Message Queue Server, consulte ayuda y soporte técnico en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="222bb-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



<span data-ttu-id="222bb-115">En el siguiente código de Visual Basic se muestra cómo llamar a la función MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="222bb-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="222bb-116">La ruta de acceso de origen del mensaje es la cola final.</span><span class="sxs-lookup"><span data-stu-id="222bb-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="222bb-117">Es la cola de mensajes inactivos, que es una cola privada de Message Queue Server y se denomina AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="222bb-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="222bb-118">Los mensajes se mueven aquí si la transacción se anula repetidamente cuando se intenta en la quinta cola de reintentos.</span><span class="sxs-lookup"><span data-stu-id="222bb-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="222bb-119">Con la herramienta de transferencia de mensajes, puede devolver el mensaje a la primera cola, que se denomina AppName.</span><span class="sxs-lookup"><span data-stu-id="222bb-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="222bb-120">Para obtener más información sobre las colas de reintento, vea [errores del servidor](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="222bb-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="222bb-121">Si los atributos de cola lo permiten, el Movedor de mensajes mueve los mensajes de forma transitoria para que los mensajes no se pierdan o se dupliquen en caso de que se produzca un error durante el traslado.</span><span class="sxs-lookup"><span data-stu-id="222bb-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="222bb-122">La herramienta conserva todas las propiedades de mensaje que se pueden conservar al mover los mensajes de una cola a otra.</span><span class="sxs-lookup"><span data-stu-id="222bb-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="222bb-123">Si los mensajes se generan mediante llamadas de componentes en cola de COM+, la utilidad del Movedor de mensajes conserva el identificador de seguridad del llamador original a medida que mueve los mensajes entre las colas.</span><span class="sxs-lookup"><span data-stu-id="222bb-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="222bb-124">Si las colas de origen y de destino son transaccionales, toda la operación se realiza de forma transitoria.</span><span class="sxs-lookup"><span data-stu-id="222bb-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="222bb-125">Si las colas de origen o de destino no son transaccionales, la operación no se ejecuta en una transacción.</span><span class="sxs-lookup"><span data-stu-id="222bb-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="222bb-126">Un error inesperado (como un bloqueo) y el reinicio de un movimiento no transaccional podría duplicar el mensaje que se está moviendo en el momento en que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="222bb-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="222bb-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="222bb-127">C/C++</span></span>

<span data-ttu-id="222bb-128">En el código de ejemplo siguiente se muestra cómo crear un objeto MessageMover, cómo establecer las propiedades necesarias y cómo iniciar la transferencia.</span><span class="sxs-lookup"><span data-stu-id="222bb-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="222bb-129">El método ErrorDescription se describe en [interpretar los códigos de error](interpreting-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="222bb-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="222bb-130">Para usar el objeto MessageMover, debe tener Message Queue Server instalado en el equipo y la aplicación especificada por AppName debe tener habilitada la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="222bb-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="222bb-131">Para obtener información acerca de cómo instalar Message Queue Server, consulte ayuda y soporte técnico en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="222bb-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



<span data-ttu-id="222bb-132">En el código de C++ siguiente se muestra cómo llamar a la función MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="222bb-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



<span data-ttu-id="222bb-133">La ruta de acceso de origen del mensaje es la cola final.</span><span class="sxs-lookup"><span data-stu-id="222bb-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="222bb-134">Es la cola de mensajes inactivos, que es una cola privada de Message Queue Server y se denomina AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="222bb-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="222bb-135">Los mensajes se mueven aquí si la transacción se anula repetidamente cuando se intenta en la quinta cola de reintentos.</span><span class="sxs-lookup"><span data-stu-id="222bb-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="222bb-136">Con la herramienta de transferencia de mensajes, puede devolver el mensaje a la primera cola, que se denomina AppName.</span><span class="sxs-lookup"><span data-stu-id="222bb-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="222bb-137">Para obtener más información sobre las colas de reintento, vea [errores del servidor](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="222bb-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="222bb-138">Si los atributos de cola lo permiten, el Movedor de mensajes mueve los mensajes de forma transitoria para que los mensajes no se pierdan o se dupliquen en caso de que se produzca un error durante el traslado.</span><span class="sxs-lookup"><span data-stu-id="222bb-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="222bb-139">La herramienta conserva todas las propiedades de mensaje que se pueden conservar al mover los mensajes de una cola a otra.</span><span class="sxs-lookup"><span data-stu-id="222bb-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="222bb-140">Si los mensajes se generan mediante llamadas de componentes en cola de COM+, la utilidad del Movedor de mensajes conserva el identificador de seguridad del llamador original a medida que mueve los mensajes entre las colas.</span><span class="sxs-lookup"><span data-stu-id="222bb-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="222bb-141">Si las colas de origen y de destino son transaccionales, toda la operación se realiza de forma transitoria.</span><span class="sxs-lookup"><span data-stu-id="222bb-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="222bb-142">Si las colas de origen o de destino no son transaccionales, la operación no se ejecuta en una transacción.</span><span class="sxs-lookup"><span data-stu-id="222bb-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="222bb-143">Un error inesperado (como un bloqueo) y el reinicio de un movimiento no transaccional podría duplicar el mensaje que se está moviendo en el momento en que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="222bb-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="222bb-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="222bb-144">Remarks</span></span>

<span data-ttu-id="222bb-145">COM+ controla las anulaciones del lado servidor (reproductor) moviendo el mensaje que no está en otra cola de "finalización", para sacarlo del camino.</span><span class="sxs-lookup"><span data-stu-id="222bb-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="222bb-146">El agente de escucha y el reproductor no pueden repetir continuamente en un mensaje que se anule.</span><span class="sxs-lookup"><span data-stu-id="222bb-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="222bb-147">En muchos casos, la transacción anulada se puede corregir realizando una acción en el servidor.</span><span class="sxs-lookup"><span data-stu-id="222bb-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="222bb-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="222bb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222bb-149">Errores de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="222bb-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 



