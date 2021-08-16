---
description: Proporciona acceso a información sobre los autores de llamadas individuales en una colección de llamadores. La colección representa la cadena de llamadas que termina con la llamada actual y cada llamador de la colección representa la identidad de un llamador.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Clase SecurityCallers (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: a494e1421e443d2a6c3663bd7fa7c15eda898079477592e8df9958a2d5b87990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915899"
---
# <a name="securitycallers-class"></a>Clase SecurityCallers

Proporciona acceso a información sobre los autores de llamadas individuales en una colección de llamadores. La colección representa la cadena de llamadas que termina con la llamada actual y cada llamador de la colección representa la identidad de un llamador. Solo los llamadores que cruzan un límite donde se comprueba la seguridad se incluyen en la cadena de llamadores. (En el entorno COM+, la seguridad se comprueba en los límites de la aplicación). El acceso a la información sobre la identidad de un llamador determinado se proporciona a través de la [**clase SecurityIdentity,**](securityidentity.md) una colección de identidades.

Solo las aplicaciones COM+ que usan la seguridad basada en roles pueden acceder a **la clase SecurityCallers.** Para obtener más información sobre los roles, vea [Administración de seguridad basada en roles.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Valor |
|------------|------------------------------------------------------|
| Interfaces | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="remarks"></a>Comentarios

No se puede crear directamente un **objeto SecurityCallers.** Para usar los métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), debe obtener una referencia a su implementación llamando a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)y suministrando \_ IID ISecurityCallContext para el *parámetro riid.* A continuación, llame a [**ISecurityCallContext::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando un elemento de contexto de llamada de seguridad que es una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller").

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. No se puede crear directamente un objeto SecurityCallers. Para usar sus propiedades, debe obtener una referencia a su implementación mediante [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). A continuación, obtenga la propiedad Item del objeto y solicite un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller").

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

