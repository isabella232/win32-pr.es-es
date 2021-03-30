---
description: Proporciona acceso a una colección de información de seguridad que representa la identidad de un llamador. Con esta clase, puede encontrar información sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de la llamada de seguridad.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity (clase) (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820431"
---
# <a name="securityidentity-class"></a>SecurityIdentity (clase)

Proporciona acceso a una colección de información de seguridad que representa la identidad de un llamador. Con esta clase, puede encontrar información sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de la llamada de seguridad. Para obtener más información sobre cómo se obtiene acceso a la información de contexto de llamadas de seguridad, vea seguridad de componentes de programación.

Solo las aplicaciones COM+ que utilizan la seguridad basada en roles pueden tener acceso a la clase **SecurityIdentity** . Para obtener más información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|--------------------------------------------------------|
| Interfaces | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Cuándo se usa

Utilice esta clase para tener acceso a los métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="remarks"></a>Observaciones

No se puede crear directamente un objeto **SecurityIdentity** . Para utilizar los métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), debe obtener una referencia a su implementación mediante una llamada a [**COGETCALLCONTEXT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), proporcionando IID \_ ISecurityCallContext para el parámetro *riid* . Después, llame a [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller"). Después, llame a [**ISecurityIdentityColl:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) para recuperar un elemento de identidad de seguridad (por ejemplo, "Name" o "AuthenticationService").

Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. No se puede crear directamente un objeto SecurityIdentity. Para usar sus propiedades, debe obtener específica a su implementación mediante [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). A continuación, obtenga la propiedad Item del objeto, solicitando un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller"). A continuación, use la propiedad Item del objeto SecurityIdentity para recuperar un elemento de identidad de seguridad (por ejemplo, "Name" o "AuthenticationService").

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

