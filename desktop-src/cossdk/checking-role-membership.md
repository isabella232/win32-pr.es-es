---
description: Comprobando la pertenencia al rol
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Comprobando la pertenencia al rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807652"
---
# <a name="checking-role-membership"></a><span data-ttu-id="db159-103">Comprobando la pertenencia al rol</span><span class="sxs-lookup"><span data-stu-id="db159-103">Checking Role Membership</span></span>

<span data-ttu-id="db159-104">Puede llamar al método [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para determinar si el llamador directo de un objeto es miembro de un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="db159-104">You can call the [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) method to determine whether an object's direct caller is a member of a particular role.</span></span> <span data-ttu-id="db159-105">Esta funcionalidad es útil cuando desea asegurarse de que no se ejecuta un determinado bloque de código, a menos que el llamador sea miembro de un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="db159-105">This functionality is useful when you want to ensure that a certain block of code is not executed unless the caller is a member of a particular role.</span></span>

<span data-ttu-id="db159-106">Por ejemplo, puede usar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para asegurarse de que las transacciones que superen una cantidad especificada, como $1000, solo las realizan los miembros de un rol de administrador.</span><span class="sxs-lookup"><span data-stu-id="db159-106">For example, you could use [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to ensure that transactions over a specified amount, such as $1000, are performed only by members of a Managers role.</span></span> <span data-ttu-id="db159-107">Si el autor de la llamada no es un administrador y la transacción es superior a $1000, no se realiza la transacción y se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="db159-107">If the caller is not a Manager and the transaction is over $1000, the transaction is not performed and an error message is displayed.</span></span>

<span data-ttu-id="db159-108">La mejor manera de tener acceso a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) es a través del objeto de contexto de llamada de seguridad, ya que puede usar la misma referencia al objeto de contexto de llamada de seguridad para obtener las propiedades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="db159-108">The preferred way to access [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) is through the security call context object because you can use the same reference to the security call context object to obtain security properties.</span></span> <span data-ttu-id="db159-109">Sin embargo, también puede tener acceso al método **IsCallerInRole** desde el objeto **ObjectContext** .</span><span class="sxs-lookup"><span data-stu-id="db159-109">However, you can also access the **IsCallerInRole** method from the **ObjectContext** object.</span></span> <span data-ttu-id="db159-110">(Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="db159-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

<span data-ttu-id="db159-111">Si va a desarrollar componentes para una aplicación de Microsoft Visual Basic, llame a la función [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) y, a continuación, use el contexto de la llamada de seguridad para llamar a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="db159-111">If you are developing components for a Microsoft Visual Basic application, you call the [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) function and then use the security call context to call [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



<span data-ttu-id="db159-112">Si está desarrollando una aplicación de C o C++, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar un puntero a la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) .</span><span class="sxs-lookup"><span data-stu-id="db159-112">If you are developing a C or C++ application, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to retrieve a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface.</span></span> <span data-ttu-id="db159-113">Después, llame a [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="db159-113">Then you call [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="db159-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db159-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db159-115">Obtener acceso a la información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="db159-115">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="db159-116">Determinar si está habilitada la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="db159-116">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="db159-117">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="db159-117">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
