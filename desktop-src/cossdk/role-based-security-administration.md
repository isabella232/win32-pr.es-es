---
description: Role-Based administración de seguridad
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973516"
---
# <a name="role-based-security-administration"></a>Role-Based administración de seguridad

La seguridad basada en roles es un servicio automático proporcionado por COM+ que le permite construir y aplicar administrativamente una directiva de control de acceso para la aplicación COM+. Con un modelo de configuración de seguridad flexible y extensible, la seguridad basada en roles ofrece una ventaja considerable sobre la aplicación de toda la seguridad dentro de los componentes y proporciona las siguientes ventajas:

-   Puede configurar la seguridad de forma administrativa mediante la herramienta administrativa Servicios de componentes o las funciones administrativas.
-   No es preciso escribir lógica relacionada con la seguridad en los componentes cuando la protección de roles en el nivel de método le proporciona un control de acceso lo suficientemente preciso.
-   No es necesario tener en cuenta la seguridad en el diseño de interfaces o componentes. En su lugar, puede establecer la seguridad método a método.
-   Puede centrarse en la estructura de la directiva de seguridad que desea aplicar y, a través de roles, esa directiva se puede expresar claramente a los administradores que implementan la aplicación.
-   Puede modificar fácilmente una directiva de seguridad para adaptarla a los requisitos de seguridad en constante evolución de una aplicación.
-   Puede crear directivas de seguridad más granulares mediante programación si es necesario, usando la seguridad basada en roles como plataforma compatible.
-   Puede aprovechar la seguridad basada en roles para realizar auditorías detalladas, ya que puede obtener información de seguridad del llamador para toda una cadena de llamadas ascendentes.

> [!Note]  
> Los usuarios del rol Administrador de la aplicación del sistema deben ser miembros del grupo de administradores locales. Además, a partir Windows Server 2003, la funcionalidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ DISABLE \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se usa en la llamada [**a CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la funcionalidad de autenticación en EOAC DISABLE AAA permite que una aplicación que se ejecuta con una cuenta con privilegios \_ (como LocalSystem) ayude a evitar que su identidad se utilice para iniciar componentes que no son de \_ confianza.

 

Consulte los temas siguientes de esta sección para obtener información sobre cómo funciona la seguridad basada en roles y los problemas que se deben tener en cuenta al usarlo para construir una directiva de seguridad para una aplicación:

-   [Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
-   [Diseño eficaz de roles](designing-roles-effectively.md)
-   [Límites de seguridad](security-boundaries.md)
-   [Información de contexto de llamada de seguridad](security-call-context-information.md)
-   [Propiedad contexto de seguridad](security-context-property.md)

Para obtener descripciones detalladas de los pasos necesarios para configurar la seguridad basada en roles para una aplicación, vea [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de la aplicación de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
