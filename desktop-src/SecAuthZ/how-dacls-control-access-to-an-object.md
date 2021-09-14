---
description: Cuando un subproceso intenta acceder a un objeto protegible, el sistema concede o deniega el acceso.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Funcionamiento de AccessCheck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071197"
---
# <a name="how-accesscheck-works"></a>Funcionamiento de AccessCheck

Cuando un subproceso intenta acceder a un objeto protegible, el sistema concede o deniega el acceso. Si el objeto no tiene una lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL), el sistema concede acceso; De lo contrario, el sistema [busca Access Control entradas](access-control-entries.md) (ACE) en la DACL del objeto que se aplican al subproceso. Cada ACE de la DACL del objeto especifica los derechos de acceso permitidos o denegados para un administrador de [confianza,](trustees.md)que puede ser una cuenta de usuario, una cuenta de grupo o una sesión [*de inicio de sesión*](/windows/desktop/SecGloss/l-gly).

## <a name="dacls"></a>DACL

El sistema compara el administrador de confianza de cada ACE con los administradores identificados en el token de [acceso del subproceso.](access-tokens.md) Un token de acceso contiene [*identificadores de*](/windows/desktop/SecGloss/s-gly) seguridad (SID) que identifican al usuario y a las cuentas de grupo a las que pertenece el usuario. Un token también contiene un [*SID de inicio de sesión*](/windows/desktop/SecGloss/l-gly) que identifica la sesión de inicio de sesión actual. Durante una comprobación de acceso, el sistema omite los SID de grupo que no están habilitados. Para obtener más información sobre los SID habilitados, deshabilitados y de solo denegación, vea [Atributos de SID en un token de acceso.](sid-attributes-in-an-access-token.md)

Normalmente, el sistema usa el [*token de acceso principal*](/windows/desktop/SecGloss/p-gly) del subproceso que solicita acceso. Sin embargo, si el subproceso suplanta a otro usuario, el sistema usa el token de [*suplantación del subproceso*](/windows/desktop/SecGloss/i-gly).

El sistema examina cada ACE en secuencia hasta que se produce uno de los siguientes eventos:

-   Una ACE con acceso denegado deniega [](access-rights-and-access-masks.md) explícitamente cualquiera de los derechos de acceso solicitados a uno de los administradores de confianza enumerados en el token de acceso del subproceso.
-   Una o varias ACE con acceso permitido para administradores de confianza que aparecen en el token de acceso del subproceso conceden explícitamente todos los derechos de acceso solicitados.
-   Se han comprobado todas las ACE y todavía hay al menos un derecho de acceso solicitado que no se ha permitido explícitamente, en cuyo caso el acceso se deniega implícitamente.

En la ilustración siguiente se muestra cómo la DACL de un objeto puede permitir el acceso a un subproceso mientras se deniega el acceso a otro.

![dacl que concede derechos de acceso diferentes a subprocesos diferentes](images/accctrl1.png)

En el caso del subproceso A, el sistema lee ACE 1 y deniega inmediatamente el acceso porque la ACE con acceso denegado se aplica al usuario en el token de acceso del subproceso. En este caso, el sistema no comprueba las ACE 2 y 3. Para el subproceso B, ACE 1 no se aplica, por lo que el sistema continúa con ACE 2, que permite el acceso de escritura, y ACE 3, que permite el acceso de lectura y ejecución.

Dado que el sistema deja de comprobar las ACE cuando se concede o deniega explícitamente el acceso solicitado, el orden de las ACE en una DACL es importante. Tenga en cuenta que si el orden ace fuera diferente en el ejemplo, el sistema podría haber concedido acceso al subproceso A. En el caso de los objetos del sistema, el sistema operativo define un orden [preferido de ACE en una DACL.](order-of-aces-in-a-dacl.md)

 

 
