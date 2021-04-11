---
description: Acelerar las transacciones mediante la notificación del objeto raíz
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Acelerar las transacciones mediante la notificación del objeto raíz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274923"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Acelerar las transacciones mediante la notificación del objeto raíz

Para utilizar eficazmente las transacciones automáticas, cada componente transaccional debe indicar que ha completado su trabajo. Cuando una instancia de objeto completa su tarea correctamente, debe establecer sus marcas coherentes y realizadas en true llamando al método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Cuando todos los objetos interiores de la transacción han llamado a **SetComplete**, la transacción puede terminarse desactivando explícitamente el objeto raíz llamando a su método **SetComplete** . Al indicar explícitamente que un objeto raíz ha completado su trabajo, puede reducir la longitud de la transacción.

Cuando se produce un error en un método de objeto transaccional, el objeto debe establecer su marca coherente en false y su marca done en true llamando al método [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) . Al llamar al método **SetAbort** , un objeto devuelve el control a su llamador y garantiza que la transacción se anula en última instancia.

Sin embargo, a menos que el objeto que llama a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) sea la raíz de la transacción, la transacción continúa ejecutándose aunque nada pueda guardarse de la anulación. Para acelerar la finalización de una transacción con errores, puede generar un error para alertar al objeto raíz para que también llame a **SetAbort**. Para finalizar, el objeto raíz debería enviar un mensaje de error a su cliente.

Aunque existen muchos enfoques diferentes que puede adoptar para controlar los errores, el enfoque debe coordinar claramente las comunicaciones entre los objetos interiores y el objeto raíz.

En los siguientes fragmentos de código de Visual Basic se muestra un enfoque para el control de errores. En el primer fragmento, un objeto interior llama a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), genera un error y genera un mensaje de error, como se indica a continuación:

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

En el segundo fragmento, el objeto raíz controla el error y pasa el mensaje a su cliente, como se indica a continuación:

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



