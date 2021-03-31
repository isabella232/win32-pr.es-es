---
title: Controlar la visibilidad de los objetos
description: Active Directory Domain Services proporcionan la capacidad de ocultar objetos de usuarios a los que se han denegado determinados derechos.
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- controlar la visibilidad de los objetos Active Directory
- Active Directory Active Directory, usar, controlar la visibilidad de los objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077551"
---
# <a name="controlling-object-visibility"></a>Controlar la visibilidad de los objetos

Active Directory Domain Services proporcionan la capacidad de ocultar objetos de usuarios a los que se han denegado determinados derechos. Si un objeto está oculto, una aplicación que se ejecuta con las credenciales de un usuario no podrá enumerar o enlazar con el objeto.

Si a un usuario se le concede el derecho de control de acceso de [**\_ \_ lista de ACTRL \_ DS \_ de ADS derecho**](/windows/win32/api/iads/ne-iads-ads_rights_enum) en un contenedor, el usuario puede ver cualquiera de los objetos secundarios del contenedor. Del mismo modo, si se deniega a un usuario el derecho de control de acceso de **\_ \_ lista de ACTRL \_ DS \_ de ADS derecho** en un contenedor, el usuario no podrá ver ninguno de los objetos secundarios del contenedor. Esto permite ocultar el contenido de los contenedores completos.

El servidor de Active Directory también se puede colocar en un modo de objeto de lista especial estableciendo el tercer carácter de la propiedad [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) en "1". El modo de objeto de lista se puede deshabilitar estableciendo el tercer carácter de la propiedad **dSHeuristics** en "0". Cuando el servidor de Active Directory está en el modo de objeto de lista, un objeto seguirá estando visible si se ha concedido al usuario el derecho de [**\_ \_ lista ad ACTRL \_ DS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) en el objeto primario. Sin embargo, si al usuario se le ha denegado el derecho **ADS \_ \_ ACTRL \_ DS \_ List** en el elemento primario, los objetos secundarios específicos podrán seguir siendo visibles si se concede al usuario el **\_ objeto de \_ \_ lista \_ de DS derecho ADS** en los objetos primarios y secundarios. El modo de objeto de lista permite al administrador del sistema conceder o denegar el acceso a objetos individuales para usuarios o grupos. El modo de objeto de lista debe usarse con moderación porque requiere que el servicio de directorio realice un número significativamente mayor de llamadas de comprobación de acceso para determinar si un objeto es visible para un usuario. Por lo tanto, puede tener un efecto negativo en el rendimiento de la exploración o la lectura de objetos desde Active Directory Domain Services.

 

 