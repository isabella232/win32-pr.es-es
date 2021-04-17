---
description: En el siguiente ejemplo de script se muestra la notificación de eventos asincrónicos y se usa el método SWbemServices.ExecNotificationQueryAsync y el objeto SWbemSink.
ms.assetid: 8beb9804-088e-4dd1-adc8-a29ca450a220
ms.tgt_platform: multiple
title: 'Ejemplo: supervisar varias consultas de eventos simultáneamente'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d70aff849cce81d6628b80f39e57a7f2430af056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706760"
---
# <a name="example-monitoring-multiple-event-queries-simultaneously"></a><span data-ttu-id="75808-103">Ejemplo: supervisar varias consultas de eventos simultáneamente</span><span class="sxs-lookup"><span data-stu-id="75808-103">Example: Monitoring Multiple Event Queries Simultaneously</span></span>

<span data-ttu-id="75808-104">En el siguiente ejemplo de script se muestra la notificación de eventos asincrónicos y se usa el método [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) y el objeto [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="75808-104">The following script example shows asynchronous event notification, making use of the [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) method and [**SWbemSink**](swbemsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="75808-105">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="75808-105">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="75808-106">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="75808-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 


```VB
Dim WithEvents sink As SWbemSink

Private Sub ExecNoteAsync_Click()

    Dim services As SWbemServices
    Dim strQuery As String
    Dim cntxt As SWbemNamedValueSet
    Set sink = New SWbemSink
    Set services = GetObject( _
        "winmgmts:{impersonationLevel=impersonate,(security)}")
    strQuery = "SELECT * FROM __InstanceCreationEvent "& _
                "WHERE TargetInstance ISA 'Win32_NTLogEvent'"
    Set cntxt = New SWbemNamedValueSet
    cntxt.Add "sinkname", "ExecNoteAsync"
    services.Security_.Privileges.Add (wbemPrivilegeSecurity)
    services.ExecNotificationQueryAsync sink, strQuery, , , , cntxt
    MsgBox "This program will asynchronously " _
        & "process Win32_NTLogEvent events."
        
End Sub

Private Sub sink_OnObjectReady( _
             ByVal objWbemObject As WbemScripting.ISWbemObject, 
             ByVal objWbemAsyncContext As _
                 WbemScripting.ISWbemNamedValueSet)
  On Error GoTo ErrorHandler
    Dim cntxt_item As WbemScripting.SWbemNamedValue

    Set cntxt_item = objWbemAsyncContext.Item("sinkname")
        
    If cntxt_item.Value = "ExecNoteAsync" Then
        MsgBox " Got event: " & objWbemObject.TargetInstance.Message
    End If

    Set objWbemObject = Nothing

    Exit Sub                                   ' Exit to avoid handler

ErrorHandler:
    MsgBox "Error number: " & Str(Err.Number) & vbNewLine & _
    "Description: " & Err.Description, vbCritical
End Sub
```



 

 



