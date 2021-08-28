---
title: Control de la visibilidad de objetos
description: Active Directory Domain Services la capacidad de ocultar objetos a usuarios a los que se les han denegado determinados derechos.
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- control de la visibilidad de objetos Active Directory
- Active Directory Active Directory , utilizando, controlando la visibilidad de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9e91701243e5c302bc417dd616171ccd52198e002a45b7f71cdd5e7b173812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021506"
---
# <a name="controlling-object-visibility"></a>Control de la visibilidad de objetos

Active Directory Domain Services la capacidad de ocultar objetos a usuarios a los que se les han denegado determinados derechos. Si un objeto está oculto, una aplicación que se ejecuta con las credenciales de un usuario no podrá enumerar ni enlazar al objeto.

Si a un usuario se le concede el derecho de control de acceso [**ADS \_ RIGHT \_ ACTRL \_ DS \_ LIST**](/windows/win32/api/iads/ne-iads-ads_rights_enum) en un contenedor, el usuario puede ver cualquiera de los objetos secundarios del contenedor. Del mismo modo, si se deniega a un usuario el derecho de control de acceso **ADS \_ RIGHT \_ ACTRL \_ DS \_ LIST** en un contenedor, el usuario no podrá ver ninguno de los objetos secundarios del contenedor. Esto permite ocultar el contenido de contenedores completos.

El Active Directory servidor también se puede colocar en un modo de objeto de lista especial estableciendo el tercer carácter de la propiedad [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) en "1". El modo de objeto de lista se puede deshabilitar estableciendo el tercer carácter de la **propiedad dSHeuristics** en "0". Cuando el servidor Active Directory está en el modo de objeto de lista, un objeto seguirá estando visible si se le ha concedido al usuario el derecho ADS [**\_ RIGHT \_ ACTRL \_ DS \_ LIST**](/windows/win32/api/iads/ne-iads-ads_rights_enum) en el objeto primario. Sin embargo, si se ha denegado al usuario el derecho **ADS \_ RIGHT \_ ACTRL \_ DS \_ LIST** en el elemento primario, se pueden hacer visibles objetos secundarios específicos si se concede al usuario el derecho **ADS RIGHT \_ \_ DS LIST \_ \_ OBJECT** en los objetos primarios y secundarios. El modo de objeto de lista permite al administrador del sistema conceder o denegar el acceso a objetos individuales para usuarios o grupos. El modo de objeto de lista debe usarse con moderación porque requiere que el servicio de directorio haga un número significativamente mayor de llamadas de comprobación de acceso para determinar si un objeto es visible para un usuario. Por lo tanto, puede tener un efecto negativo en el rendimiento de examinar o leer objetos de Active Directory Domain Services.

 

 