---
description: Usar componentes no transaccionales en una transacción
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Usar componentes no transaccionales en una transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365cf6f8e5c20f328f4308366e9a98916d9277363bba815fdbc00b5e2d8203d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991355"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>Usar componentes no transaccionales en una transacción

A menudo resulta útil colocar componentes no transaccionales en una transacción para aprovechar las propiedades [ACID](acid-properties.md) de las transacciones. Por ejemplo, si tiene componentes heredados no transaccionales que usa para actualizar contraseñas en una red, puede colocar esos componentes en una transacción para asegurarse de que las actualizaciones de contraseñas sean coherentes en toda la red.

El *objeto de contexto* de transacción es un objeto genérico que permite a los clientes no transaccionales combinar el trabajo de varios objetos COM en una sola transacción, sin necesidad de desarrollar un nuevo componente específicamente para ese propósito. A diferencia de una transacción automática, el objeto de contexto de transacción requiere que su cliente confirme o anule explícitamente la transacción.

De forma predeterminada, el valor del atributo de transacción del objeto de contexto de transacción se establece en Requerido. COM+ anula la transacción si el cliente libera el objeto de contexto de transacción sin emitir explícitamente una llamada de confirmación o anulación.

En el Visual Basic siguiente se muestra cómo un cliente no transaccional puede componer el trabajo realizado por más de un objeto en una única transacción:


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a>Limitaciones del objeto de contexto de transacción

A continuación se encuentran algunas limitaciones importantes del objeto de contexto de transacción:

-   Cuando se usa un objeto de contexto de transacción, la lógica de aplicación que combina el trabajo de varios objetos en una sola transacción está asociada a una implementación de cliente no transaccional específica y se pierden algunas ventajas de usar componentes COM. Estas ventajas perdidas incluyen las siguientes:
    -   Capacidad de reutilizar la lógica de la aplicación como parte de una transacción incluso mayor
    -   Garantía de seguridad declarativa
    -   Flexibilidad para ejecutar la lógica de forma remota desde el cliente
-   El objeto de contexto de transacción se ejecuta en proceso con el cliente no transaccional, lo que significa que COM+ debe estar disponible en el equipo cliente no transaccional. Esto podría no ser un problema, por ejemplo, cuando se usa el objeto de contexto de transacción desde una página Active Server Pages (ASP) que se ejecuta en el mismo servidor que COM+.
-   No se obtiene un contexto para el cliente no transaccional al crear un objeto de contexto de transacción. El trabajo transaccional solo se puede realizar indirectamente, a través de objetos COM creados mediante el objeto de contexto de transacción. En concreto, el cliente no transaccional no puede usar dispensadores de recursos COM+ (como ODBC) y tener el trabajo incluido en la transacción. Por ejemplo, los desarrolladores pueden estar familiarizados con la sintaxis siguiente para realizar el trabajo transaccional en sistemas de bases de datos relacionales:

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    El uso del objeto de contexto de transacción de forma similar no produce el resultado deseado:

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    La llamada a DoWork en este ejemplo no se inselecciona en una transacción. En su lugar, debe crear un componente COM que llame a DoWork, crear una instancia de objeto de ese componente mediante el objeto de contexto de transacción y, a continuación, llamar a ese objeto desde el cliente no transaccional para que el trabajo forme parte de la transacción controlada por el cliente.

 

 



