---
description: Diseñar para la seguridad
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Diseñar para la seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714842"
---
# <a name="designing-for-security"></a>Diseñar para la seguridad

La estrategia de un extremo a otro para la seguridad obviamente depende del tipo de aplicación distribuida que esté desarrollando. A continuación se muestran varias sugerencias para abordar la seguridad con respecto a la lógica de aplicación de nivel intermedio:

-   Para mejorar la eficacia y el rendimiento, autentique lo más cerca posible del usuario. Si la aplicación implica una arquitectura de lógica a base de datos de explorador a empresa, considere la posibilidad de asignar los clientes del explorador a las identidades de dominio, ejecutar la aplicación COM+ bajo identidades específicas de cada aplicación y configurar tablas en la capa de datos para que solo sean accesibles por una identidad de aplicación concreta. Este escenario de servidor de confianza es más escalable y menos problemático que el uso del DBMS para la autenticación.
-   Si está diseñando un componente que se usará en una aplicación distribuida mediante la seguridad basada en roles, puede usar la funcionalidad de [seguridad de com+](com--security.md) . Esta funcionalidad le permite llamar a métodos como [**IObjectContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) y [**IObjectContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) para ayudar a proteger los bloques de código frente al acceso no autorizado. También puede utilizar el contexto de la llamada de seguridad para obtener información sobre los llamadores de un objeto.
-   Si está diseñando un componente que se usará en una aplicación distribuida sin usar la seguridad basada en roles, la seguridad se comprueba automáticamente solo en el nivel de proceso. Los permisos de acceso al proceso determinan quién tiene acceso a la aplicación. Si necesita un control granular más preciso sobre la configuración de seguridad en el proceso o en el nivel de interfaz, utilice la funcionalidad de seguridad mediante programación proporcionada por COM.
-   Si un componente que utiliza la seguridad mediante programación de COM+ se ejecuta sin integrarse en una aplicación COM+, se producirán excepciones. Por lo tanto, si desea que este componente se integre correctamente en una aplicación que no forma parte del entorno de COM+, debe controlar todas las excepciones de manera adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseñar para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseño para la escalabilidad](designing-for-scalability.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> </dl>

 

 



