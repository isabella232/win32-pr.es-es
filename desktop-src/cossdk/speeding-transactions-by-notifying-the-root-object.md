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
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="92f90-103">Acelerar las transacciones mediante la notificación del objeto raíz</span><span class="sxs-lookup"><span data-stu-id="92f90-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="92f90-104">Para utilizar eficazmente las transacciones automáticas, cada componente transaccional debe indicar que ha completado su trabajo.</span><span class="sxs-lookup"><span data-stu-id="92f90-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="92f90-105">Cuando una instancia de objeto completa su tarea correctamente, debe establecer sus marcas coherentes y realizadas en true llamando al método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="92f90-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="92f90-106">Cuando todos los objetos interiores de la transacción han llamado a **SetComplete**, la transacción puede terminarse desactivando explícitamente el objeto raíz llamando a su método **SetComplete** .</span><span class="sxs-lookup"><span data-stu-id="92f90-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="92f90-107">Al indicar explícitamente que un objeto raíz ha completado su trabajo, puede reducir la longitud de la transacción.</span><span class="sxs-lookup"><span data-stu-id="92f90-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="92f90-108">Cuando se produce un error en un método de objeto transaccional, el objeto debe establecer su marca coherente en false y su marca done en true llamando al método [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) .</span><span class="sxs-lookup"><span data-stu-id="92f90-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="92f90-109">Al llamar al método **SetAbort** , un objeto devuelve el control a su llamador y garantiza que la transacción se anula en última instancia.</span><span class="sxs-lookup"><span data-stu-id="92f90-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="92f90-110">Sin embargo, a menos que el objeto que llama a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) sea la raíz de la transacción, la transacción continúa ejecutándose aunque nada pueda guardarse de la anulación.</span><span class="sxs-lookup"><span data-stu-id="92f90-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="92f90-111">Para acelerar la finalización de una transacción con errores, puede generar un error para alertar al objeto raíz para que también llame a **SetAbort**.</span><span class="sxs-lookup"><span data-stu-id="92f90-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="92f90-112">Para finalizar, el objeto raíz debería enviar un mensaje de error a su cliente.</span><span class="sxs-lookup"><span data-stu-id="92f90-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="92f90-113">Aunque existen muchos enfoques diferentes que puede adoptar para controlar los errores, el enfoque debe coordinar claramente las comunicaciones entre los objetos interiores y el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="92f90-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="92f90-114">En los siguientes fragmentos de código de Visual Basic se muestra un enfoque para el control de errores.</span><span class="sxs-lookup"><span data-stu-id="92f90-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="92f90-115">En el primer fragmento, un objeto interior llama a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), genera un error y genera un mensaje de error, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="92f90-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="92f90-116">En el segundo fragmento, el objeto raíz controla el error y pasa el mensaje a su cliente, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="92f90-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="92f90-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92f90-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f90-118">Administrar transacciones automáticas en COM+</span><span class="sxs-lookup"><span data-stu-id="92f90-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



