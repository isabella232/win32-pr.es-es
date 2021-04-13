---
description: El uso correcto de la Directiva de restricción de software puede hacer que su empresa sea más ágil porque proporciona un marco proactivo para evitar problemas, en lugar de un marco reactivo que se basa en la alternativa costosa de restaurar un sistema después de que se haya producido un problema. La Directiva de restricción de software se presentó con la versión de Microsoft Windows XP para ayudar a proteger los sistemas de código desconocido y posiblemente peligroso. La Directiva de restricción ofrece un mecanismo en el que solo se proporciona acceso sin restricciones a un código de confianza a los privilegios de los usuarios. El código desconocido, que podría contener virus o código que entra en conflicto con los programas instalados actualmente, solo se puede ejecutar en un entorno restringido (a menudo denominado espacio aislado) en el que no se permite el acceso a ningún privilegio de usuario que tenga en cuenta la seguridad.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Usar la Directiva de restricción de software en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3620aba8cce2859d76ba07c2fa9655dd9036bdbb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496307"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Usar la Directiva de restricción de software en COM+

El uso correcto de la Directiva de restricción de software puede hacer que su empresa sea más ágil porque proporciona un marco proactivo para evitar problemas, en lugar de un marco reactivo que se basa en la alternativa costosa de restaurar un sistema después de que se haya producido un problema. La Directiva de restricción de software se presentó con la versión de Microsoft Windows XP para ayudar a proteger los sistemas de código desconocido y posiblemente peligroso. La Directiva de restricción ofrece un mecanismo en el que solo se proporciona acceso sin restricciones a un código de confianza a los privilegios de un usuario. El código desconocido, que podría contener virus o código que entra en conflicto con los programas instalados actualmente, solo se puede ejecutar en un entorno restringido (a menudo denominado *espacio aislado*) en el que no se permite el acceso a ningún privilegio de usuario que tenga en cuenta la seguridad.

La Directiva de restricción de software depende de la asignación de niveles de confianza al código que se puede ejecutar en un sistema. Actualmente, existen dos niveles de confianza: no restringido y no permitido. Al código que tiene un nivel de confianza sin restricciones se le concede acceso no restringido a los privilegios del usuario, por lo que este nivel de confianza debe aplicarse solo al código de plena confianza. El código con un nivel de confianza no permitido no permite el acceso a ningún privilegio de usuario que tenga en cuenta la seguridad y solo puede ejecutarse en un espacio aislado que ayuda a evitar que el código sin restricciones cargue el código no permitido en su espacio de direcciones.

La configuración de la Directiva de restricción de software para un sistema se realiza a través de la herramienta administrativa Directiva de seguridad local, mientras que la configuración de la Directiva de restricción de aplicaciones COM+ individuales se realiza mediante programación o a través de la herramienta administrativa Servicios de componentes. Si no se especifica el nivel de confianza de la Directiva de restricción para una aplicación COM+, se usará la configuración de todo el sistema para determinar el nivel de confianza de la aplicación. La configuración de la Directiva de restricción de COM+ se debe coordinar cuidadosamente con la configuración de todo el sistema, ya que una aplicación COM+ que tiene un nivel de confianza sin restricciones solo puede cargar componentes con un nivel de confianza no restringido. una aplicación COM+ no permitida puede cargar componentes con cualquier nivel de confianza pero no puede tener acceso a todos los privilegios del usuario.

Además de los niveles de confianza de la Directiva de restricción de software de las aplicaciones COM+ individuales, otras dos propiedades determinan cómo se utiliza la Directiva de restricción para todas las aplicaciones COM+. Si [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) está habilitado, se comprueban los intentos de conexión a objetos en ejecución para comprobar los niveles de confianza adecuados. El objeto en ejecución no puede tener un nivel de confianza menos estricto que el objeto de cliente. Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza no permitido si el objeto de cliente tiene un nivel de confianza no restringido.

La segunda propiedad determina el modo en que la Directiva de restricción de software controla las conexiones de activación como activador. Si [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) está habilitado, el nivel de confianza configurado para el objeto de servidor se compara con el nivel de confianza del objeto de cliente y se utilizará el nivel de confianza más riguroso para ejecutar el objeto de servidor. Si SRPActivateAsActivatorChecks no está habilitado, el objeto de servidor se ejecutará con el nivel de confianza del objeto de cliente, independientemente del nivel de confianza con el que se configuró. De forma predeterminada, tanto SRPRunningObjectChecks como SRPActivateAsActivatorChecks están habilitados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Configuración de la Directiva de restricción de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> </dl>

 

 
