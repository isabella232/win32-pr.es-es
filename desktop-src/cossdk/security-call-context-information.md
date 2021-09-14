---
description: Información de contexto de llamada de seguridad
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Información de contexto de llamada de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973496"
---
# <a name="security-call-context-information"></a>Información de contexto de llamada de seguridad

La seguridad basada en roles se basa en un mecanismo general que le permite recuperar información de seguridad relacionada con todos los llamadores ascendentes de la cadena de llamadas al componente. Esta información solo está disponible cuando tiene habilitada la comprobación de roles de nivel de componente. Para obtener más información sobre cómo establecer la seguridad de nivel de componente, vea Establecer un nivel de seguridad para [las comprobaciones de acceso.](setting-a-security-level-for-access-checks.md)

Puede usar la interfaz [**ISecurityCallContext para acceder**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) a la información de contexto de llamada de seguridad mediante programación. Para obtener una descripción, vea [Seguridad de componentes mediante programación.](programmatic-component-security.md)

El contexto de llamada de seguridad se pasa cada vez que se cruza un límite de seguridad. Para las llamadas entre componentes dentro de una aplicación, que residen dentro del mismo límite de seguridad, no se pasa información de contexto de llamada. Para las llamadas entre procesos o entre aplicaciones dentro de un proceso, la información de contexto de llamada fluye a lo largo de .

Esta utilidad es especialmente útil si desea realizar auditorías y registros detallados. Puede recuperar y registrar información de seguridad para cada llamador ascendente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño eficaz de roles](designing-roles-effectively.md)
</dt> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Propiedad contexto de seguridad](security-context-property.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



