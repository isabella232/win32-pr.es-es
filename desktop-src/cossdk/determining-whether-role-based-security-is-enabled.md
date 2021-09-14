---
description: Determinar si Role-Based seguridad está habilitada
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Determinar si Role-Based seguridad está habilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358905"
---
# <a name="determining-whether-role-based-security-is-enabled"></a>Determinar si Role-Based seguridad está habilitada

Mediante el uso [**del método ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponible en el objeto de contexto de llamada de seguridad, puede determinar si la seguridad está habilitada para el objeto actual. Debe llamar a **IsSecurityEnabled antes** de usar ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para comprobar la pertenencia al rol porque **IsCallerInRole** devuelve True si la seguridad no está habilitada.

Los Visual Basic de Microsoft llaman a [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) para obtener una referencia a un objeto [**SecurityCallContext**](securitycallcontext.md) y, a continuación, llaman a [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), como se muestra en el ejemplo siguiente:


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ desarrolladores pueden llamar a [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) llamando a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obtener un puntero a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) y, a continuación, llamando a **IsSecurityEnabled**. A continuación se muestra un breve ejemplo:


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



Aunque la manera preferida de llamar a [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) es mediante el objeto de contexto de llamada de seguridad, también puede llamar a **IsSecurityEnabled** a través del contexto del objeto. (Vea [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obtener más información).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a la información de contexto de llamada de seguridad](accessing-security-call-context-information.md)
</dt> <dt>

[Comprobación de la pertenencia a roles](checking-role-membership.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 
