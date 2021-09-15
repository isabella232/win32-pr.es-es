---
description: Diseño para la seguridad
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Diseño para la seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568496"
---
# <a name="designing-for-security"></a>Diseño para la seguridad

Obviamente, la estrategia de seguridad de un extremo a otro depende del tipo de aplicación distribuida que se está desarrollando. A continuación se muestra varias sugerencias para abordar la seguridad con respecto a la lógica de aplicación de nivel intermedio:

-   Para mejorar la eficacia y el rendimiento, autentíquense lo más cerca posible del usuario. Si la aplicación implica una arquitectura de explorador a lógica de negocios a base de datos, considere la posibilidad de asignar los clientes del explorador a identidades de dominio, ejecutar la aplicación COM+ en identidades específicas de cada aplicación y configurar tablas en la capa de datos para que solo una identidad de aplicación determinada pueda acceder a ellas. Este escenario de servidor de confianza es más escalable y menos problemático que el uso del DBMS para la autenticación.
-   Si va a diseñar un componente que se usará en una aplicación distribuida mediante la seguridad basada en roles, puede usar la funcionalidad de seguridad [com+.](com--security.md) Esta funcionalidad permite llamar a métodos como [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) e [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) para ayudar a proteger los bloques de código frente al acceso no autorizado. También puede usar el contexto de llamada de seguridad para obtener información sobre los llamadores de un objeto.
-   Si va a diseñar un componente que se usará en una aplicación distribuida sin usar la seguridad basada en roles, la seguridad solo se comprueba automáticamente en el nivel de proceso. Los permisos de acceso de proceso determinan quién tiene acceso a la aplicación. Si necesita un control más preciso sobre la configuración de seguridad en el proceso o en el nivel de interfaz, use la funcionalidad de seguridad mediante programación proporcionada por COM.
-   Si un componente que usa la seguridad mediante programación de COM+ se ejecuta sin integrarse en una aplicación COM+, se producirán excepciones. Por lo tanto, si desea que este componente se integre correctamente en una aplicación que no forma parte del entorno COM+, debe controlar todas las excepciones correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseño para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseño para la escalabilidad](designing-for-scalability.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 



