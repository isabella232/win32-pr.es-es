---
title: Directiva de restricción de software
description: La configuración de la directiva de restricción de software (SRP) se introdujo con el lanzamiento de Windows XP para ayudar a proteger los sistemas frente a código desconocido y posiblemente peligroso.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23176b23be5fcf4dc45f040f53e5d8f9dfbcdf05a8aee87feabd125d05c5372d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129807"
---
# <a name="software-restriction-policy"></a>Directiva de restricción de software

La configuración de la directiva de restricción de software (SRP) se introdujo con el lanzamiento de Windows XP para ayudar a proteger los sistemas frente a código desconocido y posiblemente peligroso. El SRP proporciona un mecanismo en el que solo el código de confianza tiene acceso sin restricciones a los privilegios de un usuario. El código desconocido, que puede contener virus o código que entra en conflicto con los programas instalados actualmente, solo se puede ejecutar en un entorno restringido (a menudo denominado espacio *aislado),* donde no se permite el acceso a los privilegios de usuario que tienen en cuenta la seguridad. El uso correcto de SRP puede hacer que su negocio sea más ágil porque proporciona un marco proactivo para evitar problemas, en lugar de un marco reactivo que se basa en la costosa alternativa de restaurar un sistema después de que se haya producido un problema.

El SRP depende de la asignación de niveles de confianza al código que se puede ejecutar en un sistema. Actualmente, existen dos niveles de confianza: No restringido y No permitido. El código que tiene un nivel de confianza Sin restricciones tiene acceso sin restricciones a los privilegios del usuario, por lo que este nivel de confianza solo se debe aplicar al código de plena confianza. El código con un nivel de confianza No permitido no puede acceder a los privilegios de usuario que tienen en cuenta la seguridad y solo se puede ejecutar en un espacio aislado para que el código no restringido no pueda cargar el código no permitido en su espacio de direcciones.

La configuración de SRP de aplicaciones COM individuales se realiza a través del valor [SRPTrustLevel](srptrustlevel.md) en la clave [AppID](appid-key.md) de la aplicación en el Registro. Si no se especifica el nivel de confianza de SRP para una aplicación COM, se usa el valor predeterminado No permitido. Una aplicación COM que tiene un nivel de confianza sin restricciones tiene acceso sin restricciones a los privilegios del usuario, pero solo puede cargar componentes con un nivel de confianza sin restricciones, mientras que una aplicación COM no permitido puede cargar componentes con cualquier nivel de confianza, pero no puede acceder a ningún privilegio de usuario que tenga en cuenta la seguridad.

Además de los niveles de confianza de SRP de aplicaciones COM individuales, otras dos propiedades de SRP determinan cómo se usa SRP para todas las aplicaciones COM. Si [SRPRunningObjectChecks](srprunningobjectchecks.md) está habilitado, se comprobarán los niveles de confianza de SRP adecuados para intentar conectarse a objetos en ejecución. El objeto en ejecución no puede tener un nivel de confianza SRP menos estricto que el objeto de cliente. Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza No permitido si el objeto de cliente tiene un nivel de confianza Sin restricciones.

La segunda propiedad determina cómo el SRP controla las conexiones de activación como activador. Si [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) está habilitado, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y se usará el nivel de confianza más estricto para ejecutar el objeto de servidor. Si **SRPActivateAsActivatorChecks** no está habilitado, el objeto de servidor se ejecuta con el nivel de confianza SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que se configuró. De forma predeterminada, **SRPRunningObjectChecks y** **SRPActivateAsActivatorChecks** están habilitados.

 

 




