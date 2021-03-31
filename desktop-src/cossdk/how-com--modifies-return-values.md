---
description: Cómo modifica COM+ los valores devueltos
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Cómo modifica COM+ los valores devueltos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153204"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="36508-103">Cómo modifica COM+ los valores devueltos</span><span class="sxs-lookup"><span data-stu-id="36508-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="36508-104">COM+ nunca cambia el valor devuelto de un **HRESULT** que indica un error, como e \_ inesperado o \_ error.</span><span class="sxs-lookup"><span data-stu-id="36508-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="36508-105">Sin embargo, cuando un objeto que usa la funcionalidad de COM+ devuelve un valor **HRESULT** que indica que se ha realizado correctamente (por ejemplo \_ , S OK, s \_ false o NoError), com+ convierte a veces el **HRESULT** en un código de error de com+ antes de que vuelva al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="36508-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="36508-106">Por ejemplo, cuando una aplicación devuelve S \_ OK después de llamar a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), si el objeto es la raíz de una transacción que no se puede confirmar, el **valor HRESULT** se convierte en el contexto \_ E \_ anulado.</span><span class="sxs-lookup"><span data-stu-id="36508-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="36508-107">Cuando COM+ convierte un valor **HRESULT** , borra todos los parámetros de salida del método.</span><span class="sxs-lookup"><span data-stu-id="36508-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="36508-108">Se liberan las referencias devueltas y los valores de los punteros de objeto devueltos se establecen en **null**.</span><span class="sxs-lookup"><span data-stu-id="36508-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36508-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36508-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36508-110">Aislamiento de errores y Directiva FailFast</span><span class="sxs-lookup"><span data-stu-id="36508-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="36508-111">Buscar el origen de un error</span><span class="sxs-lookup"><span data-stu-id="36508-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="36508-112">Interpretar códigos de error</span><span class="sxs-lookup"><span data-stu-id="36508-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="36508-113">Estrategias para controlar errores en COM+</span><span class="sxs-lookup"><span data-stu-id="36508-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="36508-114">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="36508-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



