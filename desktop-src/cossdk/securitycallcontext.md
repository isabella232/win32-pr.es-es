---
description: Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: Clase SecurityCallContext (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: f0efa73ef704d77cc68b5a1193ccdc3de71b1ed0a5b8c730a2ea67474600bf5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546269"
---
# <a name="securitycallcontext-class"></a>Clase SecurityCallContext

Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto. Con esta clase, también puede averiguar si el autor de la llamada directo de un objeto es miembro de un rol determinado y si la seguridad está habilitada para el objeto.

Solo las aplicaciones COM+ que usan la seguridad basada en roles pueden acceder a **la clase SecurityCallContext.** Para obtener más información sobre los roles, vea [Administración de seguridad basada en roles.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Cuándo implementar

ESTA clase se implementa mediante COM+.



| Requisito | Valor |
|------------|------------------------------------------------------|
| Interfaces | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos [**de ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="remarks"></a>Comentarios

No se puede crear directamente un **objeto SecurityCallContext.** Para usar los métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), debe obtener una referencia a su implementación mediante una llamada a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), que proporciona IID ISecurityCallContext para el \_ parámetro *riid.*

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto SecurityCallContext se puede declarar mediante "COMSVCSLib.SecurityCallContext" como nombre de clase; se crea mediante una llamada [**a GetSecurityCallContext.**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> <dt>

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

