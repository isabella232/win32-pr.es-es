---
description: Un token restringido es un token de acceso principal o de suplantación modificado por la función CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Tokens restringidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee8e6c89915e3edd0a9206f84a0d3d5697a3cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154757"
---
# <a name="restricted-tokens"></a>Tokens restringidos

Un token restringido es un [*token de acceso*](/windows/desktop/SecGloss/a-gly) [*principal*](/windows/desktop/SecGloss/p-gly) o de suplantación modificado por la función [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . Un [*proceso*](/windows/desktop/SecGloss/p-gly) o subproceso de suplantación que se ejecuta en el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) de un token restringido está restringido en su capacidad de obtener acceso a objetos protegibles o realizar operaciones con privilegios. La función **CreateRestrictedToken** puede restringir un token de las siguientes maneras:

-   Quite los [privilegios](privileges.md) del token.
-   Aplique el atributo de solo denegación a los SID en el token para que no se puedan usar para tener acceso a los objetos protegidos. Para obtener más información sobre el atributo de solo denegación, vea [atributos SID en un token de acceso](sid-attributes-in-an-access-token.md).
-   Especifique una lista de SID restrictivos, que puede limitar el acceso a los objetos protegibles.

El sistema utiliza la lista de restricciones de SID cuando comprueba el acceso del token a un objeto protegible. Cuando un proceso o subproceso restringido intenta tener acceso a un objeto protegible, el sistema realiza dos comprobaciones de acceso: una con los SID habilitados del token y otra mediante la lista de SID restrictivos. El acceso se concede solo si ambas comprobaciones de acceso permiten los derechos de acceso solicitados. Para obtener más información sobre las comprobaciones de acceso, vea [cómo los DACL controlan el acceso a un objeto](how-dacls-control-access-to-an-object.md).

Puede usar un [*token primario*](/windows/desktop/SecGloss/p-gly) restringido en una llamada a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Normalmente, el proceso que llama a **CreateProcessAsUser** debe tener el \_ privilegio de nombre de ASSIGNPRIMARYTOKEN se \_ , que normalmente solo se mantiene en el código del sistema o en los servicios que se ejecutan en la cuenta LocalSystem. Sin embargo, si la llamada de **CreateProcessAsUser** especifica una versión restringida del token principal del llamador, este privilegio no es necesario. Esto permite a las aplicaciones normales crear procesos restringidos.

También puede usar un [*token de suplantación*](/windows/desktop/SecGloss/i-gly) Primary Primary o Primary en la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Para determinar si un token tiene una lista de SID restrictivos, llame a la función [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) .

> [!Note]  
> Las aplicaciones que usan tokens restringidos deben ejecutar la aplicación restringida en equipos de escritorio distintos del escritorio predeterminado. Esto es necesario para evitar un ataque por parte de una aplicación restringida, mediante **SendMessage** o **PostMessage**, en aplicaciones sin restricciones en el escritorio predeterminado. Si es necesario, cambie entre equipos de escritorio para los fines de su aplicación.

 

 

 
