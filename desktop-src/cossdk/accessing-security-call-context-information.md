---
description: Cuando se utiliza la seguridad basada en roles, el objeto de contexto de llamada de seguridad se puede utilizar para tener acceso a la información de seguridad sobre la llamada actual.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Obtener acceso a la información de contexto de llamada de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275028"
---
# <a name="accessing-security-call-context-information"></a>Obtener acceso a la información de contexto de llamada de seguridad

Cuando se utiliza la seguridad basada en roles, el objeto de contexto de llamada de seguridad se puede utilizar para tener acceso a la información de seguridad sobre la llamada actual.

Las siguientes colecciones de propiedades están disponibles en el objeto de contexto de llamada de seguridad:

-   [SecurityCallContext (colección)](#securitycallcontext-collection)
-   [Colección SecurityCallers](#securitycallers-collection)
-   [SecurityIdentity (colección)](#securityidentity-collection)
-   [Temas relacionados](#related-topics)

## <a name="securitycallcontext-collection"></a>SecurityCallContext (colección)



| Propiedad                          | Descripción                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | Número de llamadores de la cadena de llamadas.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Nivel de autenticación menos seguro de todos los llamadores de la cadena.<br/>                                                          |
| Los llamadores<br/>                | Información sobre la identidad de los llamadores de nivel superior, en forma de una colección [**SecurityCallers**](securitycallers.md) .<br/> |
| DirectCaller<br/>           | Llamador que llamó directamente al objeto (sin ningún llamador que intervenga). <br/>                                                  |
| OriginalCaller<br/>         | Llamador que originó la cadena de llamadas al objeto. <br/>                                                               |



 

Para obtener más información sobre cómo usar esta colección, los desarrolladores de Microsoft Visual Basic deben ver la clase [**SecurityCallContext**](securitycallcontext.md) . Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="securitycallers-collection"></a>Colección SecurityCallers

La colección [**SecurityCallers**](securitycallers.md) representa a los llamadores que se pueden recuperar mediante un índice entre 0 y 1 menor que NumCallers, ambos incluidos. Cada llamador se representa mediante un objeto [**SecurityIdentity**](securityidentity.md) .

Para obtener más información sobre esta colección, los desarrolladores de Visual Basic deberían ver la clase [**SecurityCallers**](securitycallers.md) . Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="securityidentity-collection"></a>SecurityIdentity (colección)



| Propiedad                         | Descripción                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | El identificador de seguridad para el autor de la llamada.<br/>                                                                                                                   |
| AccountName<br/>           | Nombre de cuenta del autor de la llamada.<br/>                                                                                                                           |
| AuthenticationService<br/> | Servicio de autenticación usado, como NTLMSSP, Kerberos o SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | El nivel de autenticación utilizado, que representa la cantidad de protección utilizada al comunicarse con el objeto.<br/>                                         |
| ImpersonationLevel<br/>    | Nivel de suplantación establecido por el cliente, si se ha utilizado la suplantación. Este nivel indica la cantidad de autoridad proporcionada al servidor por el cliente. <br/> |



 

Para obtener más información sobre esta colección, los desarrolladores de Visual Basic deberían ver la clase [**SecurityIdentity**](securityidentity.md) . Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comprobando la pertenencia al rol](checking-role-membership.md)
</dt> <dt>

[Determinar si está habilitada la seguridad de Role-Based](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 




