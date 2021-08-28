---
description: Terminación de una transacción automática mediante una llamada a SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Terminación de una transacción automática mediante una llamada a SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d84d18b45309d750864d514728b8e23a3326e5edeba0bf144105bcbaa4797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499665"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Terminación de una transacción automática mediante una llamada a SetComplete

Para usar las transacciones automáticas de forma eficaz, cada componente transaccional debe indicar que ha completado su trabajo. Cuando una instancia de objeto completa correctamente su tarea, debe establecer sus marcas coherentes y realizadas en True llamando al método [**IObjectContext::SetComplete,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) que se expone a través de la interfaz [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) y el [**objeto ObjectContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext)

La manera más eficaz de completar una transacción automática es desactivar explícitamente el objeto raíz mediante el [**método SetComplete.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) Al indicar explícitamente que un objeto raíz ha completado su trabajo, puede reducir la longitud de la transacción.

En el Visual Basic ejemplo siguiente se muestra cómo indicar que un objeto transaccional ha completado correctamente su trabajo:


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

[Marcas coherentes y realizadas](consistent-and-done-flags.md)
</dt> <dt>

[Administración de transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



