---
description: Comprobación de la pertenencia a roles
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Comprobación de la pertenencia a roles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973572"
---
# <a name="checking-role-membership"></a>Comprobación de la pertenencia a roles

Puede llamar al método [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para determinar si el llamador directo de un objeto es miembro de un rol determinado. Esta funcionalidad es útil cuando se desea asegurarse de que un determinado bloque de código no se ejecuta a menos que el autor de la llamada sea miembro de un rol determinado.

Por ejemplo, podría usar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para asegurarse de que las transacciones sobre una cantidad especificada, como 1000 USD, solo las realizan los miembros de un rol De administradores. Si el autor de la llamada no es un administrador y la transacción supera los 1000 USD, la transacción no se realiza y se muestra un mensaje de error.

La manera preferida de acceder a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) es a través del objeto de contexto de llamada de seguridad porque puede usar la misma referencia al objeto de contexto de llamada de seguridad para obtener propiedades de seguridad. Sin embargo, también puede acceder al **método IsCallerInRole** desde el **objeto ObjectContext.** (Vea [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obtener más información).

Si va a desarrollar componentes para una aplicación de Microsoft Visual Basic, llame a la función [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) y, a continuación, use el contexto de llamada de seguridad para llamar a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), como se muestra en el ejemplo siguiente:


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



Si va a desarrollar una aplicación de C o C++, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar un puntero a la [**interfaz ISecurityCallContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) A continuación, [**llame a ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), como se muestra en el ejemplo siguiente:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a la información de contexto de llamada de seguridad](accessing-security-call-context-information.md)
</dt> <dt>

[Determinar si la Role-Based seguridad está habilitada](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 
