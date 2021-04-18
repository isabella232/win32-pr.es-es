---
description: Finalizar una transacción automática llamando a SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Finalizar una transacción automática llamando a SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666179"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Finalizar una transacción automática llamando a SetComplete

Para utilizar eficazmente las transacciones automáticas, cada componente transaccional debe indicar que ha completado su trabajo. Cuando una instancia de objeto completa su tarea correctamente, debe establecer sus marcas de coherencia y realización en true llamando al método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , que se expone a través de la interfaz [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) y del objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

La forma más eficaz de completar una transacción automática es desactivar explícitamente el objeto raíz mediante el método [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Al indicar explícitamente que un objeto raíz ha completado su trabajo, puede reducir la longitud de la transacción.

En el siguiente Visual Basic ejemplo se muestra cómo indicar que un objeto transaccional ha completado su trabajo correctamente:


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Marcas de coherencia y de realización](consistent-and-done-flags.md)
</dt> <dt>

[Administrar transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



