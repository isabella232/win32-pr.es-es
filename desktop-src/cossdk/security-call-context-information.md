---
description: Información de contexto de llamada de seguridad
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Información de contexto de llamada de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275087"
---
# <a name="security-call-context-information"></a>Información de contexto de llamada de seguridad

La seguridad basada en roles se basa en un mecanismo general que permite recuperar información de seguridad con respecto a todos los llamadores ascendentes en la cadena de llamadas al componente. Esta información solo está disponible cuando tiene habilitada la comprobación de roles de nivel de componente. Para obtener más información sobre cómo establecer la seguridad de nivel de componente, vea [establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).

Puede utilizar la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) para tener acceso a la información de contexto de llamadas de seguridad mediante programación. Para obtener una descripción, vea [seguridad de componentes de programación](programmatic-component-security.md).

El contexto de la llamada de seguridad se pasa a cada vez que se cruza un límite de seguridad. En el caso de las llamadas entre los componentes de una aplicación, que residen dentro del mismo límite de seguridad, no se pasa ninguna información de contexto de llamada. En el caso de las llamadas entre procesos o entre aplicaciones dentro de un proceso, los flujos de información del contexto de llamada se transmiten.

Esta característica es especialmente útil si desea realizar auditorías y registros detallados. Puede recuperar y registrar información de seguridad para cada llamador de nivel superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar roles de forma eficaz](designing-roles-effectively.md)
</dt> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Propiedad de contexto de seguridad](security-context-property.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



