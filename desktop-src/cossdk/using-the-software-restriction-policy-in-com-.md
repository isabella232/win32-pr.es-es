---
description: El uso correcto de la directiva de restricción de software puede hacer que su negocio sea más ágil porque proporciona un marco proactivo para evitar problemas, en lugar de un marco reactivo que se basa en la costosa alternativa de restaurar un sistema después de que se haya producido un problema. La directiva de restricción de software se introdujo con la versión de Microsoft Windows XP para ayudar a proteger los sistemas frente a código desconocido y posiblemente peligroso. La directiva de restricción proporciona un mecanismo en el que solo el código de confianza tiene acceso sin restricciones a los privilegios de los usuarios. El código desconocido, que puede contener virus o código que entra en conflicto con los programas instalados actualmente, solo se puede ejecutar en un entorno restringido (a menudo denominado espacio aislado) donde no se permite el acceso a los privilegios de usuario que tienen en cuenta la seguridad.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Uso de la directiva de restricción de software en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e823d794cccf590ddf9ffd8fcb6f7982eb1543368e400ab3632601ec3a2b96e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304941"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Uso de la directiva de restricción de software en COM+

El uso correcto de la directiva de restricción de software puede hacer que su negocio sea más ágil porque proporciona un marco proactivo para evitar problemas, en lugar de un marco reactivo que se basa en la costosa alternativa de restaurar un sistema después de que se haya producido un problema. La directiva de restricción de software se introdujo con la versión de Microsoft Windows XP para ayudar a proteger los sistemas frente a código desconocido y posiblemente peligroso. La directiva de restricción proporciona un mecanismo en el que solo el código de confianza tiene acceso sin restricciones a los privilegios de un usuario. El código desconocido, que puede contener virus o código que entra en conflicto con los programas instalados actualmente, solo se puede ejecutar en un entorno restringido (a menudo denominado espacio *aislado),* donde no se permite el acceso a los privilegios de usuario que tienen en cuenta la seguridad.

La directiva de restricción de software depende de la asignación de niveles de confianza al código que se puede ejecutar en un sistema. Actualmente, existen dos niveles de confianza: Sin restricciones y No permitido. El código que tiene un nivel de confianza Sin restricciones tiene acceso sin restricciones a los privilegios del usuario, por lo que este nivel de confianza solo se debe aplicar al código de plena confianza. No se permite que el código con un nivel de confianza No permitido acceda a los privilegios de usuario que tengan en cuenta la seguridad y solo se puede ejecutar en un espacio aislado que ayude a evitar que el código no restringido cargue el código no permitido en su espacio de direcciones.

La configuración de la directiva de restricción de software para un sistema se realiza a través de la herramienta administrativa Directiva de seguridad local, mientras que la configuración de la directiva de restricción de aplicaciones COM+ individuales se realiza mediante programación o a través de la herramienta administrativa Servicios de componentes. Si no se especifica el nivel de confianza de la directiva de restricción para una aplicación COM+, la configuración de todo el sistema se usará para determinar el nivel de confianza de la aplicación. La configuración de la directiva de restricción de COM+ debe coordinarse cuidadosamente con la configuración de todo el sistema, ya que una aplicación COM+ que tenga un nivel de confianza sin restricciones solo puede cargar componentes con un nivel de confianza Sin restricciones. Una aplicación COM+ no permitido puede cargar componentes con cualquier nivel de confianza, pero no puede acceder a todos los privilegios del usuario.

Además de los niveles de confianza de la directiva de restricción de software de aplicaciones COM+ individuales, otras dos propiedades determinan cómo se usa la directiva de restricción para todas las aplicaciones COM+. Si [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) está habilitado, los intentos de conectarse a objetos en ejecución se comprobarán para obtener los niveles de confianza adecuados. El objeto en ejecución no puede tener un nivel de confianza menos estricto que el objeto de cliente. Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza No permitido si el objeto de cliente tiene un nivel de confianza Sin restricciones.

La segunda propiedad determina cómo controla la directiva de restricción de software las conexiones de activación como activador. Si [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) está habilitado, el nivel de confianza configurado para el objeto de servidor se compara con el nivel de confianza del objeto cliente y el nivel de confianza más estricto se usará para ejecutar el objeto de servidor. Si SRPActivateAsActivatorChecks no está habilitado, el objeto de servidor se ejecutará con el nivel de confianza del objeto cliente independientemente del nivel de confianza con el que se configuró. De forma predeterminada, SRPRunningObjectChecks y SRPActivateAsActivatorChecks están habilitados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Configuración de la directiva de restricción de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de varios niveles](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> </dl>

 

 
