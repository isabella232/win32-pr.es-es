---
description: Administración de la seguridad de Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Administración de la seguridad de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539183"
---
# <a name="role-based-security-administration"></a>Administración de la seguridad de Role-Based

La seguridad basada en roles es un servicio automático proporcionado por COM+ que permite construir y aplicar de forma administrativa una directiva de control de acceso para la aplicación COM+. Con un modelo de configuración de seguridad flexible y extensible, la seguridad basada en roles ofrece una ventaja considerable en cuanto a la aplicación de toda la seguridad dentro de los componentes y proporciona las siguientes ventajas:

-   Puede configurar la seguridad de forma administrativa mediante la herramienta administrativa Servicios de componentes o las funciones administrativas.
-   No es necesario escribir lógica relacionada con la seguridad en los componentes cuando la protección de roles en el nivel de método proporciona un control de acceso suficiente.
-   No tiene que factorizar la seguridad en el diseño de interfaces o componentes. En su lugar, puede establecer la seguridad para cada método.
-   Puede centrarse en la estructura de la Directiva de seguridad que desea aplicar y, a través de los roles, la Directiva se puede expresar claramente en los administradores que implementan la aplicación.
-   Puede modificar fácilmente una directiva de seguridad para adaptarse a los requisitos de seguridad en constante evolución de una aplicación.
-   Puede crear directivas de seguridad más granulares mediante programación si es necesario, mediante el uso de la seguridad basada en roles como plataforma auxiliar.
-   Puede aprovechar la seguridad basada en roles para realizar auditorías detalladas, ya que puede obtener información de seguridad del autor de la llamada para toda una cadena de llamadas de nivel superior.

> [!Note]  
> Los usuarios de la función Administrador de la aplicación del sistema deben ser miembros del grupo local Administradores. Además, a partir de Windows Server 2003, la capacidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ Disable \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se utiliza en la llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la capacidad de autenticación en EOAC \_ deshabilitar \_ AAA permite que una aplicación que se ejecuta en una cuenta con privilegios (como LocalSystem) ayude a evitar que se use su identidad para iniciar componentes que no son de confianza.

 

Vea los temas siguientes en esta sección para obtener información acerca de cómo funcionan la seguridad basada en roles y los problemas que se deben tener en cuenta cuando se usa para construir una directiva de seguridad para una aplicación:

-   [Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
-   [Diseñar roles de forma eficaz](designing-roles-effectively.md)
-   [Límites de seguridad](security-boundaries.md)
-   [Información de contexto de llamada de seguridad](security-call-context-information.md)
-   [Propiedad de contexto de seguridad](security-context-property.md)

Para obtener descripciones detalladas de los pasos necesarios para configurar la seguridad basada en roles de una aplicación, consulte Configuración de la [seguridad de Role-Based](configuring-role-based-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Usar la Directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
