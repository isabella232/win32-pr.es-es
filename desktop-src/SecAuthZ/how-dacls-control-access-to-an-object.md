---
description: Cuando un subproceso intenta tener acceso a un objeto protegible, el sistema concede o deniega el acceso.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Cómo funciona AccessCheck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553113"
---
# <a name="how-accesscheck-works"></a>Cómo funciona AccessCheck

Cuando un subproceso intenta tener acceso a un objeto protegible, el sistema concede o deniega el acceso. Si el objeto no tiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL), el sistema concede acceso; de lo contrario, el sistema busca [entradas de Access Control](access-control-entries.md) (ACE) en la DACL del objeto que se aplican al subproceso. Cada ACE de la DACL del objeto especifica los derechos de acceso permitidos o denegados para un [Administrador de confianza](trustees.md), que puede ser una cuenta de usuario, una cuenta de grupo o una [*sesión de inicio*](/windows/desktop/SecGloss/l-gly)de sesión.

## <a name="dacls"></a>DACL

El sistema compara el administrador de confianza de cada ACE con los que confían identificados en el [token de acceso](access-tokens.md)del subproceso. Un token de acceso contiene los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que identifican al usuario y a las cuentas de grupo a las que pertenece el usuario. Un token también contiene un [*SID de inicio de sesión*](/windows/desktop/SecGloss/l-gly) que identifica la sesión de inicio de sesión actual. Durante una comprobación de acceso, el sistema omite los SID de grupo que no están habilitados. Para obtener más información sobre los SID habilitados, deshabilitados y de solo denegación, consulte [atributos de SID en un token de acceso](sid-attributes-in-an-access-token.md).

Normalmente, el sistema utiliza el [*token de acceso principal*](/windows/desktop/SecGloss/p-gly) del subproceso que solicita acceso. Sin embargo, si el subproceso está suplantando a otro usuario, el sistema utiliza el [*token de suplantación*](/windows/desktop/SecGloss/i-gly)del subproceso.

El sistema examina cada ACE en secuencia hasta que se produce uno de los siguientes eventos:

-   Una ACE de acceso denegado deniega explícitamente cualquiera de los [derechos de acceso](access-rights-and-access-masks.md) solicitados a uno de los que se enumeran en el token de acceso del subproceso.
-   Una o varias ACE de acceso permitido para los confianzas enumerados en el token de acceso del subproceso conceden explícitamente todos los derechos de acceso solicitados.
-   Todas las ACE se han comprobado y todavía hay al menos un derecho de acceso solicitado que no se ha permitido explícitamente, en cuyo caso el acceso se deniega implícitamente.

En la ilustración siguiente se muestra cómo la DACL de un objeto puede permitir el acceso a un subproceso a la vez que se deniega el acceso a otro.

![DACL que concede derechos de acceso diferentes a distintos subprocesos](images/accctrl1.png)

En el caso del subproceso A, el sistema lee ACE 1 y deniega inmediatamente el acceso porque la ACE de acceso denegado se aplica al usuario en el token de acceso del subproceso. En este caso, el sistema no comprueba las ACE 2 y 3. En el caso del subproceso B, ACE 1 no es aplicable, por lo que el sistema continúa con ACE 2, que permite el acceso de escritura y ACE 3, que permite el acceso de lectura y ejecución.

Dado que el sistema detiene la comprobación de ACE cuando se concede o se deniega explícitamente el acceso solicitado, es importante el orden de las ACE en una DACL. Tenga en cuenta que si el orden de ACE era diferente en el ejemplo, el sistema podría haber concedido acceso al subproceso a. En el caso de los objetos del sistema, el sistema operativo define el [orden preferido de las ACE en una DACL](order-of-aces-in-a-dacl.md).

 

 
