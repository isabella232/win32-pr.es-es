---
description: Al usar la seguridad basada en roles en la aplicación COM+ que contiene el componente, tiene acceso a la funcionalidad de seguridad mediante programación desde dentro del componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Seguridad de componentes mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966931"
---
# <a name="programmatic-component-security"></a>Seguridad de componentes mediante programación

Al usar la seguridad basada en roles en la aplicación COM+ que contiene el componente, tiene acceso a la funcionalidad de seguridad mediante programación desde dentro del componente. Puede comprobar la pertenencia a roles para determinar si se ejecutan determinadas secciones de código, puede acceder a la información de seguridad mediante el objeto de contexto de llamada de seguridad y puede determinar si la seguridad está habilitada para la llamada actual. Puede realizar todas estas tareas mediante una referencia a un objeto [**SecurityCallContext**](securitycallcontext.md) (para aplicaciones de Microsoft Visual Basic) o un puntero a la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (para aplicaciones de C y Microsoft Visual C++).

Para obtener más información sobre la seguridad basada en roles mediante programación, vea los temas siguientes en esta sección:

-   [Comprobación de la pertenencia a roles](checking-role-membership.md)
-   [Determinar si Role-Based seguridad está habilitada](determining-whether-role-based-security-is-enabled.md)
-   [Acceso a la información de contexto de llamada de seguridad](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Suplantación y características de seguridad COM

Si el componente se usa en una aplicación COM+ que no usa la seguridad basada en roles, la comprobación de roles mediante programación y la información de contexto de llamada de seguridad no están disponibles. Sin embargo, puede usar la funcionalidad de seguridad mediante programación proporcionada por COM. Para obtener más información, vea [Seguridad en COM.](/windows/desktop/com/security-in-com)

Aunque puede usar la mayor parte de la funcionalidad de seguridad proporcionada por COM, no puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) desde un componente que forma parte de una aplicación COM+ porque el suplente en el que se ejecuta la aplicación COM+ llama a **CoInitializeSecurity.** Sin embargo, puede llamar a otras funciones de seguridad, como [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), que recupera información sobre el cliente.

En concreto, cuando necesite usar la identidad del cliente para acceder a algún recurso(por ejemplo, acceder a un archivo protegido por un descriptor de seguridad o propagar la identidad del cliente a través de una base de datos), puede realizar la suplantación mediante programación. Para obtener más información sobre cuándo y cómo hacerlo, vea [Suplantación y delegación de cliente.](client-impersonation-and-delegation.md)

## <a name="testing-security-functionality"></a>Probar la funcionalidad de seguridad

Si usa la seguridad mediante programación de COM+ en el componente, debe integrarlo en una aplicación COM+ cuando esté listo para probar la funcionalidad de seguridad del componente. Si un componente que usa la seguridad mediante programación de COM+ se ejecuta sin integrarse en una aplicación COM+, se producirán excepciones. Por lo tanto, si desea asegurarse de que este componente también sea capaz de integrarse correctamente en una aplicación que no forma parte del entorno COM+, debe asegurarse de que estas excepciones se controlan correctamente.

## <a name="documenting-security-requirements"></a>Documentación de los requisitos de seguridad

Si está escribiendo un componente independiente para aplicaciones COM+ que usan la seguridad basada en roles, debe documentar el componente para que la seguridad se pueda configurar correctamente cuando el componente esté integrado en una aplicación COM+. Por ejemplo, debe identificar los roles que se deben agregar y explicar a qué métodos e interfaces se debe asignar cada rol. Además, si se llama a un método como IsCallerInRole("Teller"), debe describir la funcionalidad a la que solo tienen acceso los tellers. También debe especificar si se requiere un rol para ayudar a proteger el acceso a todo el componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de varios niveles](multi-tier-application-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
