---
description: Dado que una aplicación de biblioteca COM+ está hospedada por otro proceso, que puede tener su propia configuración de seguridad, la seguridad de las aplicaciones de biblioteca requiere una consideración especial.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Seguridad de la aplicación de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9fa2d03f21707af42fa108cb9c4ecbce6d2a352ea03714961a0eef4f028119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813524"
---
# <a name="library-application-security"></a>Seguridad de la aplicación de biblioteca

Dado que una aplicación de biblioteca COM+ está hospedada por otro proceso, que puede tener su propia configuración de seguridad, la seguridad de las aplicaciones de biblioteca requiere una consideración especial.

Las restricciones siguientes se aplican a la seguridad de las aplicaciones de biblioteca:

-   Las aplicaciones de biblioteca se ejecutan bajo el token de seguridad del proceso de cliente en lugar de bajo su propia identidad de usuario. Solo tienen tantos privilegios como tiene el cliente.
-   Las aplicaciones de biblioteca no controlan la seguridad de nivel de proceso. No se agregará ningún usuario en roles al descriptor de seguridad para el proceso. La única manera de que una aplicación de biblioteca realice sus propias comprobaciones de acceso es usar la seguridad de nivel de componente. (Consulte [Límites de seguridad).](security-boundaries.md)
-   Las aplicaciones de biblioteca se pueden configurar para participar o no en la autenticación del proceso de host, habilitando o deshabilitando la autenticación. (Consulte [Habilitación de la autenticación para una aplicación de biblioteca).](enabling-authentication-for-a-library-application.md)
-   Las aplicaciones de biblioteca no pueden establecer un nivel de suplantación; usan el del proceso de host.

## <a name="using-library-applications-to-limit-application-privilege"></a>Usar aplicaciones de biblioteca para limitar los privilegios de aplicación

En algunos casos, es posible que desee configurar una aplicación específicamente como una aplicación de biblioteca para que se ejecute bajo la identidad del proceso de hospedaje. Esto limita fundamentalmente la aplicación para que solo pueda acceder a los recursos a los que puede acceder su cliente, el proceso de host. Los subprocesos en los que se ejecutan los componentes de la aplicación de biblioteca usarán el token de proceso de forma predeterminada y, por tanto, cuando realicen llamadas fuera de la aplicación o accedan a recursos como archivos guardados con un descriptor de seguridad, parecerán ser el cliente. En el caso de las aplicaciones que realizan un trabajo confidencial, esta puede ser una manera fácil de controlar el ámbito de sus acciones.

## <a name="effectively-securing-library-applications"></a>Protección eficaz de las aplicaciones de biblioteca

Hay consideraciones especiales a la hora de configurar la seguridad basada en roles y la autenticación de las aplicaciones de biblioteca para que se realicen según lo previsto. Para obtener más información, [vea Configuring Security for Library Applications](configuring-security-for-library-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



