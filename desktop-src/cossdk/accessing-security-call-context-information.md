---
description: Cuando se usa la seguridad basada en roles, se puede usar el objeto de contexto de llamada de seguridad para acceder a la información de seguridad sobre la llamada actual.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Acceso a la información de contexto de llamada de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073033"
---
# <a name="accessing-security-call-context-information"></a>Acceso a la información de contexto de llamada de seguridad

Cuando se usa la seguridad basada en roles, se puede usar el objeto de contexto de llamada de seguridad para acceder a la información de seguridad sobre la llamada actual.

Las siguientes colecciones de propiedades están disponibles en el objeto de contexto de llamada de seguridad:

-   [Colección SecurityCallContext](#securitycallcontext-collection)
-   [Colección SecurityCallers](#securitycallers-collection)
-   [Colección SecurityIdentity](#securityidentity-collection)
-   [Temas relacionados](#related-topics)

## <a name="securitycallcontext-collection"></a>Colección SecurityCallContext



| Propiedad.                          | Descripción                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | Número de autores de llamadas en la cadena de llamadas.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Nivel de autenticación menos seguro de todos los llamadores de la cadena.<br/>                                                          |
| Llamadores<br/>                | Información sobre la identidad de los autores de llamadas ascendentes, en forma de una [**colección SecurityCallers.**](securitycallers.md)<br/> |
| DirectCaller<br/>           | Llamador que llamó al objeto directamente (sin autores de llamadas que intervendres). <br/>                                                  |
| OriginalCaller<br/>         | Llamador que originó la cadena de llamadas al objeto . <br/>                                                               |



 

Para obtener más información sobre cómo usar esta colección, los desarrolladores Visual Basic Microsoft deben ver la [**clase SecurityCallContext.**](securitycallcontext.md) Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityCallContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)

## <a name="securitycallers-collection"></a>Colección SecurityCallers

La [**colección SecurityCallers**](securitycallers.md) representa los llamadores que se pueden recuperar mediante un índice entre 0 y 1 menos que NumCallers, ambos incluidos. Cada llamador se representa mediante un [**objeto SecurityIdentity.**](securityidentity.md)

Para obtener más información sobre esta colección, Visual Basic desarrolladores deben ver la [**clase SecurityCallers.**](securitycallers.md) Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="securityidentity-collection"></a>Colección SecurityIdentity



| Propiedad.                         | Descripción                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | Identificador de seguridad del autor de la llamada.<br/>                                                                                                                   |
| AccountName<br/>           | Nombre de cuenta del autor de la llamada.<br/>                                                                                                                           |
| AuthenticationService<br/> | El servicio de autenticación utilizado, como NTLMSSP, Kerberos o SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | Nivel de autenticación utilizado, que representa la cantidad de protección utilizada al comunicarse con el objeto .<br/>                                         |
| ImpersonationLevel<br/>    | Nivel de suplantación establecido por el cliente, si se usó la suplantación. Este nivel indica la cantidad de autoridad que el cliente ha dado al servidor. <br/> |



 

Para obtener más información sobre esta colección, Visual Basic desarrolladores deben ver la [**clase SecurityIdentity.**](securityidentity.md) Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityIdentityColl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comprobación de la pertenencia a roles](checking-role-membership.md)
</dt> <dt>

[Determinar si Role-Based seguridad está habilitada](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 




