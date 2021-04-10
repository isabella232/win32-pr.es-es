---
description: Determinar si está habilitada la seguridad de Role-Based
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Determinar si está habilitada la seguridad de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153463"
---
# <a name="determining-whether-role-based-security-is-enabled"></a><span data-ttu-id="ef7de-103">Determinar si está habilitada la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="ef7de-103">Determining Whether Role-Based Security Is Enabled</span></span>

<span data-ttu-id="ef7de-104">Mediante el método [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponible en el objeto de contexto de llamada de seguridad, puede determinar si la seguridad está habilitada para el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="ef7de-104">By using the [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) method available from the security call context object, you can determine whether security is enabled for the current object.</span></span> <span data-ttu-id="ef7de-105">Debe llamar a **IsSecurityEnabled** antes de usar ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para comprobar la pertenencia al rol porque **IsCallerInRole** devuelve true si la seguridad no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ef7de-105">You should call **IsSecurityEnabled** before you use ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to check role membership because **IsCallerInRole** returns True if security is not enabled.</span></span>

<span data-ttu-id="ef7de-106">Los desarrolladores de Microsoft Visual Basic llaman a [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) para obtener una referencia a un objeto [**SecurityCallContext**](securitycallcontext.md) y, a continuación, llaman a [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ef7de-106">Microsoft Visual Basic developers call [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) to obtain a reference to a [**SecurityCallContext**](securitycallcontext.md) object and then call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), as shown in the following example:</span></span>


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



<span data-ttu-id="ef7de-107">Microsoft Visual C++ los desarrolladores pueden llamar a [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) llamando a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obtener un puntero a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) y llamando a **IsSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="ef7de-107">Microsoft Visual C++ developers can call [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) and then calling **IsSecurityEnabled**.</span></span> <span data-ttu-id="ef7de-108">A continuación se muestra un breve ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ef7de-108">A brief example follows:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



<span data-ttu-id="ef7de-109">Aunque la mejor manera de llamar a [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) es usar el objeto de contexto de llamada de seguridad, también puede llamar a **IsSecurityEnabled** a través del contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="ef7de-109">Although the preferred way to call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) is by using the security call context object, you can also call **IsSecurityEnabled** through the object context.</span></span> <span data-ttu-id="ef7de-110">(Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="ef7de-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef7de-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef7de-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef7de-112">Obtener acceso a la información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="ef7de-112">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="ef7de-113">Comprobando la pertenencia al rol</span><span class="sxs-lookup"><span data-stu-id="ef7de-113">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="ef7de-114">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="ef7de-114">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
