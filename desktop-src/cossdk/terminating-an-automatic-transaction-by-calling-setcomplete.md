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
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="12016-103">Finalizar una transacción automática llamando a SetComplete</span><span class="sxs-lookup"><span data-stu-id="12016-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="12016-104">Para utilizar eficazmente las transacciones automáticas, cada componente transaccional debe indicar que ha completado su trabajo.</span><span class="sxs-lookup"><span data-stu-id="12016-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="12016-105">Cuando una instancia de objeto completa su tarea correctamente, debe establecer sus marcas de coherencia y realización en true llamando al método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , que se expone a través de la interfaz [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) y del objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .</span><span class="sxs-lookup"><span data-stu-id="12016-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="12016-106">La forma más eficaz de completar una transacción automática es desactivar explícitamente el objeto raíz mediante el método [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="12016-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="12016-107">Al indicar explícitamente que un objeto raíz ha completado su trabajo, puede reducir la longitud de la transacción.</span><span class="sxs-lookup"><span data-stu-id="12016-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="12016-108">En el siguiente Visual Basic ejemplo se muestra cómo indicar que un objeto transaccional ha completado su trabajo correctamente:</span><span class="sxs-lookup"><span data-stu-id="12016-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="12016-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12016-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12016-110">Marcas de coherencia y de realización</span><span class="sxs-lookup"><span data-stu-id="12016-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="12016-111">Administrar transacciones automáticas en COM+</span><span class="sxs-lookup"><span data-stu-id="12016-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



