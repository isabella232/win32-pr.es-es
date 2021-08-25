---
description: En ocasiones, se produce una situación en la que un mensaje no se puede entregar correctamente a su destino previsto, normalmente debido a un problema con el sistema o la configuración.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Control de errores en componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314ff367e656043746bb34bcb28b6c5a3dc8db9b86b58a482af45f684fb658c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991087"
---
# <a name="handling-errors-in-queued-components"></a>Control de errores en componentes en cola

En ocasiones, se produce una situación en la que un mensaje no se puede entregar correctamente a su destino previsto, normalmente debido a un problema con el sistema o la configuración. Por ejemplo, el mensaje podría dirigirse a una cola que no existe o es posible que la cola de destino no esté en estado de recepción. El motor de mensajes es una herramienta que mueve todos los mensajes de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) con errores de una cola a otra para que se puedan reinterio. La utilidad de mover mensajes es un objeto de Automation que se puede invocar con un VBScript.

## <a name="components-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

El código de ejemplo siguiente muestra cómo crear un objeto MessageMover, establecer las propiedades necesarias e iniciar la transferencia. Para usarlo desde Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.

> [!Note]  
> Para usar el objeto MessageMover, debe tener Message Queuing instalado en el equipo y la aplicación especificada por AppName debe tener habilitada la cola. Para obtener información sobre cómo instalar Message Queuing, vea Ayuda y soporte técnico en el **menú** Inicio.

 


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



En el Visual Basic siguiente se muestra cómo llamar a la función MyMessageMover.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



La ruta de acceso de origen del mensaje es la cola de reposo final. Es la cola de mensajes fallidos, que es una cola privada de Message Queuing y se denomina AppName \_ deadqueue. Los mensajes se mueven aquí si la transacción se anula repetidamente cuando se intenta en la quinta cola de reintentos. Con la herramienta de mover mensajes, puede volver a mover el mensaje a la primera cola, que se denomina AppName. Para obtener más información sobre las colas de reintento, vea [Errores del lado servidor.](server-side-errors.md)

Si los atributos de cola lo permiten, el motor de mensajes mueve los mensajes de forma transitoria para que los mensajes no se pierdan ni dupliquen en caso de error durante el traslado. La herramienta conserva todas las propiedades del mensaje que se pueden conservar al mover mensajes de una cola a otra.

Si las llamadas a componentes en cola de COM+ generan los mensajes, la utilidad de mover mensajes conserva el identificador de seguridad del autor de la llamada original a medida que mueve los mensajes entre colas. Si las colas de origen y de destino son transaccionales, toda la operación se realiza de forma transitoria. Si las colas de origen o destino no son transaccionales, la operación no se ejecuta en una transacción. Un error inesperado (como un bloqueo) y el reinicio de un movimiento no transaccional podrían duplicar el mensaje que se mueve en el momento del error.

## <a name="cc"></a>C/C++

El código de ejemplo siguiente muestra cómo crear un objeto MessageMover, establecer las propiedades necesarias e iniciar la transferencia. El método ErrorDescription se describe en [Interpretación de códigos de error](interpreting-error-codes.md).

> [!Note]  
> Para usar el objeto MessageMover, debe tener Message Queuing instalado en el equipo y la aplicación especificada por AppName debe tener habilitada la cola. Para obtener información sobre cómo instalar Message Queuing, vea Ayuda y soporte técnico en el **menú** Inicio.

 


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



El siguiente código de C++ muestra cómo llamar a la función MyMessageMover.


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



La ruta de acceso de origen del mensaje es la cola de reposo final. Es la cola de mensajes fallidos, que es una cola privada de Message Queuing y se denomina AppName \_ deadqueue. Los mensajes se mueven aquí si la transacción se anula repetidamente cuando se intenta en la quinta cola de reintentos. Con la herramienta de mover mensajes, puede volver a mover el mensaje a la primera cola, que se denomina AppName. Para obtener más información sobre las colas de reintento, vea [Errores del lado servidor.](server-side-errors.md)

Si los atributos de cola lo permiten, el motor de mensajes mueve los mensajes de forma transitoria para que los mensajes no se pierdan ni dupliquen en caso de error durante el traslado. La herramienta conserva todas las propiedades del mensaje que se pueden conservar al mover mensajes de una cola a otra.

Si las llamadas a componentes en cola de COM+ generan los mensajes, la utilidad de mover mensajes conserva el identificador de seguridad del autor de la llamada original a medida que mueve los mensajes entre colas. Si las colas de origen y de destino son transaccionales, toda la operación se realiza de forma transitoria. Si las colas de origen o destino no son transaccionales, la operación no se ejecuta en una transacción. Un error inesperado (como un bloqueo) y el reinicio de un movimiento no transaccional podrían duplicar el mensaje que se mueve en el momento del error.

## <a name="remarks"></a>Comentarios

COM+ controla las anulaciones del lado servidor (reproductor) moviendo el mensaje que está fallando en una cola de "reposo final" diferente, para que se salga del camino. El agente de escucha y el reproductor no pueden recorrer continuamente un mensaje que se anula. En muchos casos, la transacción anulada se puede solucionar tomando medidas en el servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de componentes en cola](queued-components-errors.md)
</dt> </dl>

 

 



