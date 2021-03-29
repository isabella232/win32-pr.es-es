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
# <a name="checking-role-membership"></a>Comprobando la pertenencia al rol

Puede llamar al método [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para determinar si el llamador directo de un objeto es miembro de un rol determinado. Esta funcionalidad es útil cuando desea asegurarse de que no se ejecuta un determinado bloque de código, a menos que el llamador sea miembro de un rol determinado.

Por ejemplo, puede usar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para asegurarse de que las transacciones que superen una cantidad especificada, como $1000, solo las realizan los miembros de un rol de administrador. Si el autor de la llamada no es un administrador y la transacción es superior a $1000, no se realiza la transacción y se muestra un mensaje de error.

La mejor manera de tener acceso a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) es a través del objeto de contexto de llamada de seguridad, ya que puede usar la misma referencia al objeto de contexto de llamada de seguridad para obtener las propiedades de seguridad. Sin embargo, también puede tener acceso al método **IsCallerInRole** desde el objeto **ObjectContext** . (Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obtener más información).

Si va a desarrollar componentes para una aplicación de Microsoft Visual Basic, llame a la función [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) y, a continuación, use el contexto de la llamada de seguridad para llamar a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), tal como se muestra en el ejemplo siguiente:


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



Si está desarrollando una aplicación de C o C++, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar un puntero a la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) . Después, llame a [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), tal como se muestra en el ejemplo siguiente:


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

[Obtener acceso a la información de contexto de llamada de seguridad](accessing-security-call-context-information.md)
</dt> <dt>

[Determinar si está habilitada la seguridad de Role-Based](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 
