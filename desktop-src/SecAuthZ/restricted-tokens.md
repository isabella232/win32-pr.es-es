---
description: Un token restringido es un token de acceso principal o de suplantación que ha sido modificado por la función CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Tokens restringidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f63402997d9e1304ca75ca117554ce52c3aa727f44b3b8316c28e1ecfcea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912013"
---
# <a name="restricted-tokens"></a>Tokens restringidos

Un token restringido es un token [*de*](/windows/desktop/SecGloss/p-gly) acceso principal o de [*suplantación*](/windows/desktop/SecGloss/a-gly) que ha sido modificado por la [**función CreateRestrictedToken.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) Un [*proceso*](/windows/desktop/SecGloss/p-gly) o suplantación [](/windows/desktop/SecGloss/s-gly) de subproceso que se ejecuta en el contexto de seguridad de un token restringido está restringido en su capacidad para acceder a objetos protegibles o realizar operaciones con privilegios. La **función CreateRestrictedToken** puede restringir un token de las maneras siguientes:

-   Quite [los privilegios](privileges.md) del token.
-   Aplique el atributo de solo denegación a los SID del token para que no se puedan usar para acceder a objetos protegidos. Para obtener más información sobre el atributo de solo denegación, vea [Atributos de SID en un token de acceso.](sid-attributes-in-an-access-token.md)
-   Especifique una lista de SID de restricción, que puede limitar el acceso a objetos protegibles.

El sistema usa la lista de SID de restricción cuando comprueba el acceso del token a un objeto protegible. Cuando un proceso o subproceso restringido intenta acceder a un objeto protegible, el sistema realiza dos comprobaciones de acceso: una con los SID habilitados del token y otra con la lista de SID de restricción. El acceso solo se concede si ambas comprobaciones de acceso permiten los derechos de acceso solicitados. Para obtener más información sobre las comprobaciones de acceso, vea [Cómo controlan las DACL el acceso a un objeto](how-dacls-control-access-to-an-object.md).

Puede usar un [*token*](/windows/desktop/SecGloss/p-gly) principal restringido en una llamada a la [**función CreateProcessAsUser.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Normalmente, el proceso que llama a **CreateProcessAsUser** debe tener el privilegio SE ASSIGNPRIMARYTOKEN NAME, que normalmente solo lo mantiene el código del sistema o los servicios que se ejecutan en la cuenta \_ \_ LocalSystem. Sin embargo, si **la llamada a CreateProcessAsUser** especifica una versión restringida del token principal del autor de la llamada, este privilegio no es necesario. Esto permite a las aplicaciones normales crear procesos restringidos.

También puede usar un token principal o de [*suplantación*](/windows/desktop/SecGloss/i-gly) restringido en la [**función ImpersonateLoggedOnUser.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)

Para determinar si un token tiene una lista de SID de restricción, llame a la [**función IsTokenRestricted.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)

> [!Note]  
> Las aplicaciones que usan tokens restringidos deben ejecutar la aplicación restringida en escritorios distintos del escritorio predeterminado. Esto es necesario para evitar un ataque por parte de una aplicación restringida, mediante **SendMessage** o **PostMessage**, para aplicaciones sin restricciones en el escritorio predeterminado. Si es necesario, cambie entre los escritorios para los fines de la aplicación.

 

 

 
