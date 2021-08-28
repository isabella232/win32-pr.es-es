---
description: Proporciona acceso a una colección de información de seguridad que representa la identidad de un autor de la llamada. Con esta clase, puede averiguar sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de llamada de seguridad.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: Clase SecurityIdentity (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: d16139ccf60a22ebfb4cf609e734e0b8df3285ef9ddb1804657313900a3ea05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305481"
---
# <a name="securityidentity-class"></a>Clase SecurityIdentity

Proporciona acceso a una colección de información de seguridad que representa la identidad de un autor de la llamada. Con esta clase, puede averiguar sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de llamada de seguridad. Para obtener más información sobre cómo se accede a la información de contexto de llamada de seguridad, vea Seguridad de componentes mediante programación.

Solo las aplicaciones COM+ que usan la seguridad basada en roles pueden acceder a **la clase SecurityIdentity.** Para obtener más información sobre los roles, vea [Administración de seguridad basada en roles.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Cuándo implementar

ESTA clase se implementa mediante COM+.



| Requisito | Valor |
|------------|--------------------------------------------------------|
| Interfaces | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos [**de ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="remarks"></a>Comentarios

No se puede crear directamente un **objeto SecurityIdentity.** Para usar los métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), debe obtener una referencia a su implementación mediante una llamada a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), que proporciona IID ISecurityCallContext para el \_ parámetro *riid.* A continuación, llame a [**ISecurityCallContext::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando un elemento de contexto de llamada de seguridad que es una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller"). A continuación, llame a [**ISecurityIdentityColl::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) para recuperar un elemento de identidad de seguridad (como "Name" o "AuthenticationService").

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. No se puede crear directamente un objeto SecurityIdentity. Para usar sus propiedades, debe obtener una referencia a su implementación mediante [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). A continuación, obtenga la propiedad Item del objeto y solicite un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller"). A continuación, use la propiedad Item del objeto SecurityIdentity para recuperar un elemento de identidad de seguridad (como "Name" o "AuthenticationService").

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

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

