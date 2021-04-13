---
description: Dado que otro proceso hospeda una aplicación de biblioteca COM+, que puede tener su propia configuración de seguridad, la seguridad de las aplicaciones de biblioteca requiere una consideración especial.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Seguridad de aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538716"
---
# <a name="library-application-security"></a>Seguridad de aplicaciones de biblioteca

Dado que otro proceso hospeda una aplicación de biblioteca COM+, que puede tener su propia configuración de seguridad, la seguridad de las aplicaciones de biblioteca requiere una consideración especial.

Las siguientes restricciones se aplican a la seguridad de la aplicación de biblioteca:

-   Las aplicaciones de biblioteca se ejecutan en el token de seguridad del proceso de cliente en lugar de en su propia identidad de usuario. Solo tienen los privilegios que tiene el cliente.
-   Las aplicaciones de biblioteca no controlan la seguridad de nivel de proceso. No se agregarán usuarios en roles al descriptor de seguridad para el proceso. La única manera de que una aplicación de biblioteca realice sus propias comprobaciones de acceso es usar la seguridad de nivel de componente. (Vea [límites de seguridad](security-boundaries.md)).
-   Las aplicaciones de biblioteca se pueden configurar para participar o no en la autenticación del proceso de host, habilitando o deshabilitando la autenticación. (Consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)).
-   Las aplicaciones de biblioteca no pueden establecer un nivel de suplantación; usan el del proceso de host.

## <a name="using-library-applications-to-limit-application-privilege"></a>Usar aplicaciones de biblioteca para limitar el privilegio de aplicación

En algunos casos, puede que desee configurar una aplicación específicamente como una aplicación de biblioteca para que se ejecute bajo la identidad del proceso de hospedaje. Esto limita fundamentalmente la aplicación para que pueda tener acceso solo a los recursos a los que puede tener acceso el cliente, el proceso de host. Los subprocesos en los que se ejecutan los componentes de la aplicación de biblioteca usarán el token de proceso de forma predeterminada y, por lo tanto, cuando realicen llamadas fuera de la aplicación o los recursos de acceso, como los archivos protegidos con un descriptor de seguridad, parecerá que son el cliente. En el caso de las aplicaciones que realizan trabajo confidencial, puede ser una forma sencilla de controlar el ámbito de sus acciones.

## <a name="effectively-securing-library-applications"></a>Proteger eficazmente aplicaciones de biblioteca

Hay algunas consideraciones especiales para configurar la seguridad basada en roles y la autenticación para las aplicaciones de biblioteca, de modo que funcionen según lo previsto. Para obtener más información, consulte [configuración de la seguridad para aplicaciones de biblioteca](configuring-security-for-library-applications.md).

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

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Usar la Directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



