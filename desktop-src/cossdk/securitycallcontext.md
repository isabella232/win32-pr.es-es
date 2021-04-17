---
description: Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: SecurityCallContext (clase) (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717433"
---
# <a name="securitycallcontext-class"></a>SecurityCallContext (clase)

Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto. Con esta clase, también puede averiguar si el llamador directo de un objeto es miembro de un rol determinado y si la seguridad está habilitada para el objeto.

Solo las aplicaciones COM+ que utilizan la seguridad basada en roles pueden tener acceso a la clase **SecurityCallContext** . Para obtener más información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|------------------------------------------------------|
| Interfaces | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Cuándo se usa

Utilice esta clase para tener acceso a los métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="remarks"></a>Observaciones

No se puede crear directamente un objeto **SecurityCallContext** . Para utilizar los métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), debe obtener una referencia a su implementación llamando a [**COGETCALLCONTEXT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), proporcionando IID \_ ISecurityCallContext para el parámetro *riid* .

Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto SecurityCallContext puede declararse con "COMSVCSLib. SecurityCallContext" como nombre de clase; se crea llamando a [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).

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

[**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> <dt>

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

