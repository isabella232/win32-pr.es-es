---
description: La seguridad basada en roles se usa para establecer una directiva de autorización, que determina qué cliente o clientes deben permitir y con qué autoridad. Está decidiendo quién debe ser capaz de realizar las acciones y obtener acceso a los recursos.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Uso de roles para la autorización de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ae748ddfec438a79e3d0440a00ed7c2f672aed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153190"
---
# <a name="using-roles-for-client-authorization"></a>Uso de roles para la autorización de cliente

La seguridad basada en roles se usa para establecer una directiva de autorización, que determina qué cliente o clientes deben permitir y con qué autoridad. Está decidiendo quién debe ser capaz de realizar las acciones y obtener acceso a los recursos.

Los roles facilitan esto actuando como un mecanismo de control de acceso que se invoca cada vez que un usuario intenta tener acceso a cualquier recurso de la aplicación. Un rol es básicamente una lista de usuarios, más concretamente, una categoría simbólica de usuarios que comparten el mismo privilegio de seguridad. Cuando asigna un rol a un recurso de aplicación, se le concede permiso de acceso para ese recurso a quien sea miembro de ese rol.

Por lo tanto, puede definir un privilegio de seguridad muy determinado declarándolo como un rol y asignando después el rol a recursos específicos. Cuando se implementa la aplicación, el administrador del sistema puede rellenar el rol con usuarios y grupos de usuarios reales. Cuando se ejecuta la aplicación, COM+ aplicará las comprobaciones de rol.

Fundamentalmente, los roles ayudan a proteger el código, es decir, los métodos a los que pueden llamar los clientes de una aplicación COM+. La pertenencia al rol se comprueba cada vez que un cliente intenta llamar a un método expuesto por un componente en una aplicación. Si el llamador está en un rol asignado al método llamado, o recurso, la llamada se realiza correctamente; de lo contrario, se produce un error.

## <a name="declarative-role-based-security"></a>Seguridad de Role-Based declarativa

Con la seguridad basada en roles declarativo, se declaran roles de forma administrativa mediante la herramienta administrativa Servicios de componentes o las funciones administrativas, y se asignan de forma administrativa a los recursos de la aplicación. Dónde y cómo se establece la seguridad declarativa determinará dónde se dibujan los límites de seguridad para la aplicación. Para obtener más información, consulte [límites de seguridad](security-boundaries.md).

Puede asignar un rol determinado a toda la aplicación, a un componente determinado, a una interfaz determinada de un componente o a un método determinado en una interfaz. Las asignaciones de roles se heredan de la cadena de inclusión natural, es decir, si se asigna un rol a un componente, se asigna implícitamente a cada interfaz y método expuesto por ese componente.

Con la disponibilidad de las asignaciones de roles de nivel de método, puede proteger eficazmente los componentes y las interfaces que no se han diseñado pensando en la seguridad. Sin embargo, si los propios métodos no son protegibles con asignaciones de roles declarativos, puede que tenga que realizar la comprobación de roles mediante programación. Por lo general, es conveniente tener en cuenta la seguridad al decidir cómo factorizar la funcionalidad empresarial a través de métodos; de lo contrario, podría haber agregado el código relacionado con la seguridad en el último minuto.

Para ver los procedimientos detallados para establecer la seguridad basada en roles, consulte Configuración de la [seguridad de Role-Based](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Seguridad mediante programación

En algunas circunstancias, puede que desee colocar la lógica de seguridad en los componentes mientras sigue usando la seguridad basada en roles. Es posible que no pueda, o elija no, factorizar todas las decisiones de acceso a través de los métodos. Por ejemplo, puede tener un recurso de aplicación privada, quizás una base de datos determinada, que desea permitir que solo algunos autores de llamadas de un método tengan acceso a la vez que excluyen otros. O bien, puede tener un único método TransferMoney y desea restringir algunos llamadores limitando la cantidad que se pueden transferir.

En tales circunstancias, puede realizar la comprobación de roles en el código. Se proporciona una API simple, lo que le permite comprobar si la seguridad está activada y si un llamador o un usuario determinado se encuentra en un rol determinado. Esta funcionalidad solo está disponible cuando está habilitada la seguridad basada en roles. Esto significa que puede seguir aprovechando la seguridad declarativa basada en roles donde es suficiente y, a continuación, puede ampliarla mediante programación a un nivel de granularidad más fino cuando sea necesario.

Además, cuando se utiliza la seguridad basada en roles, se tiene acceso mediante programación a la información relativa a todos los llamadores ascendentes en la cadena de llamadas al componente. Esto es especialmente útil si desea mantener una pista de auditoría detallada.

Para obtener descripciones sobre cómo realizar comprobaciones de roles en el código y cómo obtener acceso a la información de contexto de llamadas de seguridad, vea [seguridad de componentes de programación](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorización y autenticación

La autorización tiene la certeza de que está seguro de que los clientes son realmente quienes dicen ser. La comprobación de la identidad del cliente se controla por separado por un servicio de autenticación. Sin autenticación, básicamente se permite a los autores de llamadas en el sistema de honor. Para obtener descripciones de la autenticación a medida que afecta a las aplicaciones COM+, consulte [autenticación del cliente](client-authentication.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar roles de forma eficaz](designing-roles-effectively.md)
</dt> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Propiedad de contexto de seguridad](security-context-property.md)
</dt> </dl>

 

 



