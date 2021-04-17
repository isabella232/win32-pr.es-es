---
title: Directiva de restricción de software
description: La configuración de la Directiva de restricción de software (SRP) se incorporó con la versión de Windows XP para ayudar a proteger los sistemas de código desconocido y posiblemente peligroso.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97bf42cd949127e9012580ec16379cf36a95353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704611"
---
# <a name="software-restriction-policy"></a>Directiva de restricción de software

La configuración de la Directiva de restricción de software (SRP) se incorporó con la versión de Windows XP para ayudar a proteger los sistemas de código desconocido y posiblemente peligroso. El SRP proporciona un mecanismo en el que solo se proporciona acceso sin restricciones a un código de confianza a los privilegios de un usuario. El código desconocido, que podría contener virus o código que entra en conflicto con los programas instalados actualmente, solo se puede ejecutar en un entorno restringido (a menudo denominado *espacio aislado*) en el que no se permite el acceso a ningún privilegio de usuario que tenga en cuenta la seguridad. El uso correcto del SRP puede hacer que su empresa sea más ágil porque proporciona un marco proactivo para evitar problemas, en lugar de un marco reactivo que se basa en la alternativa costosa de restaurar un sistema después de que se haya producido un problema.

El SRP depende de la asignación de niveles de confianza al código que se puede ejecutar en un sistema. Actualmente, existen dos niveles de confianza: no restringido y no permitido. Al código que tiene un nivel de confianza sin restricciones se le concede acceso no restringido a los privilegios del usuario, por lo que este nivel de confianza debe aplicarse solo al código de plena confianza. El código con un nivel de confianza no permitido no permite el acceso a ningún privilegio de usuario que tenga en cuenta la seguridad y solo puede ejecutarse en un espacio aislado para que el código sin restricciones no pueda cargar el código no permitido en su espacio de direcciones.

La configuración de SRP de aplicaciones COM individuales se realiza a través del valor [SRPTrustLevel](srptrustlevel.md) de la clave [AppID](appid-key.md) de la aplicación en el registro. Si no se especifica el nivel de confianza de SRP para una aplicación COM, se usa el valor predeterminado de no permitido. Una aplicación COM que tiene un nivel de confianza sin restricciones tiene acceso sin restricciones a los privilegios del usuario, pero solo puede cargar componentes con un nivel de confianza no restringido, mientras que una aplicación COM no permitida puede cargar componentes con cualquier nivel de confianza pero no puede tener acceso a ningún privilegio de usuario confidencial de seguridad.

Además de los niveles de confianza de SRP de las aplicaciones COM individuales, otras dos propiedades de SRP determinan cómo se utiliza el SRP para todas las aplicaciones COM. Si [SRPRunningObjectChecks](srprunningobjectchecks.md) está habilitado, se comprueban los intentos de conexión a objetos en ejecución para comprobar los niveles de confianza de SRP correspondientes. El objeto en ejecución no puede tener un nivel de confianza SRP menos estricto que el objeto cliente. Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza no permitido si el objeto de cliente tiene un nivel de confianza no restringido.

La segunda propiedad determina cómo controla el SRP las conexiones de activación como activador. Si [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) está habilitado, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y se utilizará el nivel de confianza más riguroso para ejecutar el objeto de servidor. Si **SRPActivateAsActivatorChecks** no está habilitado, el objeto de servidor se ejecuta con el nivel de confianza de SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que se configuró. De forma predeterminada, tanto **SRPRunningObjectChecks** como **SRPActivateAsActivatorChecks** están habilitados.

 

 




