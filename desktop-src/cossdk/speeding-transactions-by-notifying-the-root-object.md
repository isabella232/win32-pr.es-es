---
description: Acelerar transacciones notificando al objeto raíz
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Acelerar transacciones notificando al objeto raíz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361647"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Acelerar transacciones notificando al objeto raíz

Para usar las transacciones automáticas de forma eficaz, cada componente transaccional debe indicar que ha completado su trabajo. Cuando una instancia de objeto completa correctamente su tarea, debe establecer sus marcas coherentes y realizadas en True llamando al [**método IObjectContext::SetComplete.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) Cuando todos los objetos interiores de la transacción han llamado **a SetComplete**, la transacción se puede finalizar desactivando explícitamente el objeto raíz llamando a su **método SetComplete.** Al indicar explícitamente que un objeto raíz ha completado su trabajo, puede reducir la longitud de la transacción.

Cuando se produce un error en un método de objeto transaccional, el objeto debe establecer su marca coherente en False y su marca done en True llamando al método [**IObjectContext::SetAbort.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) Al llamar al **método SetAbort,** un objeto devuelve el control a su autor de la llamada y garantiza que la transacción se anula en última instancia.

Sin embargo, a menos que el objeto que llama a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) sea la raíz de la transacción, la transacción continúa en ejecución aunque nada pueda evitar que finalmente se anule. Para acelerar la terminación de una transacción con error, puede generar un error para alertar al objeto raíz de que también llame a **SetAbort**. Para finalizar, el objeto raíz debe enviar un mensaje de error a su cliente.

Aunque hay muchos enfoques diferentes que puede tomar para controlar los errores, el enfoque debe coordinar claramente las comunicaciones entre los objetos interiores y el objeto raíz.

Los siguientes fragmentos Visual Basic código muestran un enfoque para el control de errores. En el primer fragmento, un objeto interior llama a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), genera un error y genera un mensaje de error, como se indica a continuación:

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

[Administración de transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



