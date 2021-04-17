---
description: Cuando se utiliza la seguridad basada en roles en la aplicación COM+ que contiene el componente, se tiene acceso a la funcionalidad de seguridad mediante programación desde dentro del componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Seguridad de componentes mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705321"
---
# <a name="programmatic-component-security"></a>Seguridad de componentes mediante programación

Cuando se utiliza la seguridad basada en roles en la aplicación COM+ que contiene el componente, se tiene acceso a la funcionalidad de seguridad mediante programación desde dentro del componente. Puede comprobar la pertenencia al rol para determinar si se ejecutan determinadas secciones de código, puede tener acceso a la información de seguridad mediante el objeto de contexto de llamada de seguridad, y puede determinar si la seguridad está habilitada para la llamada actual. Puede realizar todas estas tareas mediante una referencia a un objeto [**SecurityCallContext**](securitycallcontext.md) (para aplicaciones de Microsoft Visual Basic) o un puntero a la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (para aplicaciones de C y Microsoft Visual C++).

Para obtener más información sobre la seguridad basada en roles mediante programación, vea los temas siguientes en esta sección:

-   [Comprobando la pertenencia al rol](checking-role-membership.md)
-   [Determinar si está habilitada la seguridad de Role-Based](determining-whether-role-based-security-is-enabled.md)
-   [Obtener acceso a la información de contexto de llamada de seguridad](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Características de suplantación y seguridad COM

Si el componente se utiliza en una aplicación COM+ que no usa la seguridad basada en roles, la comprobación de roles mediante programación y la información de contexto de llamada de seguridad no están disponibles. Sin embargo, puede utilizar la funcionalidad de seguridad mediante programación proporcionada por COM. Para obtener más información, vea [seguridad en com](/windows/desktop/com/security-in-com).

Aunque puede usar la mayoría de las funciones de seguridad proporcionadas por COM, no se puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) desde un componente que forma parte de una aplicación com+ porque el suplente al que se ejecuta la aplicación com+ llama a **CoInitializeSecurity** . Sin embargo, puede llamar a otras funciones de seguridad, como [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), que recupera información sobre el cliente.

En concreto, cuando necesite usar la identidad del cliente para tener acceso a algún recurso (por ejemplo, tener acceso a un archivo protegido por un descriptor de seguridad o propagar la identidad del cliente a través de una base de datos), puede realizar la suplantación mediante programación. Para obtener más información sobre cuándo y cómo hacerlo, vea [suplantación y delegación de cliente](client-impersonation-and-delegation.md).

## <a name="testing-security-functionality"></a>Probar la funcionalidad de seguridad

Si utiliza la seguridad de programación de COM+ en el componente, debe integrar el componente en una aplicación COM+ cuando esté listo para probar la funcionalidad de seguridad del componente. Si un componente que utiliza la seguridad mediante programación de COM+ se ejecuta sin integrarse en una aplicación COM+, se producirán excepciones. Por lo tanto, si desea asegurarse de que este componente también sea capaz de integrarse correctamente en una aplicación que no forma parte del entorno de COM+, debe asegurarse de que estas excepciones se controlen correctamente.

## <a name="documenting-security-requirements"></a>Documentar los requisitos de seguridad

Si está escribiendo un componente independiente para aplicaciones COM+ que usan la seguridad basada en roles, debe documentar el componente para que la seguridad se pueda configurar correctamente cuando el componente se integre en una aplicación COM+. Por ejemplo, debe identificar los roles que se deben agregar y explicar a qué métodos e interfaces se debe asignar cada rol. Además, si se llama a un método como IsCallerInRole ("Teller"), debe describir la funcionalidad a la que solo los cajeros tienen acceso. También debe especificar si un rol es necesario para ayudar a proteger el acceso a todo el componente.

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

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Usar la Directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
