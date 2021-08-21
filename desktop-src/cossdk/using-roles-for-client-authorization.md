---
description: La seguridad basada en roles se usa para establecer una directiva de autorización, determinando qué cliente o clientes se deben permitir y con qué autoridad. Está decidiendo quién debe ser capaz de realizar qué acciones y acceder a qué recursos.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Uso de roles para la autorización de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a808abc08d5360ba0b7fae0a7c31af80a4cab28c43e6014076c549204e6f28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499654"
---
# <a name="using-roles-for-client-authorization"></a>Uso de roles para la autorización de cliente

La seguridad basada en roles se usa para establecer una directiva de autorización, determinando qué cliente o clientes se deben permitir y con qué autoridad. Está decidiendo quién debe ser capaz de realizar qué acciones y acceder a qué recursos.

Los roles facilitan esta acción actuando como un mecanismo de control de acceso invocado cada vez que un usuario intenta acceder a cualquier recurso de aplicación. Un rol es básicamente una lista de usuarios, más concretamente, una categoría simbólica de usuarios que comparten el mismo privilegio de seguridad. Al asignar un rol a un recurso de aplicación, se concede permiso de acceso para ese recurso a quien sea miembro de ese rol.

Por lo tanto, puede definir un privilegio de seguridad muy determinado si lo declara como un rol y, a continuación, asigna el rol a recursos específicos. Cuando se implementa la aplicación, el administrador del sistema puede rellenar el rol con usuarios y grupos de usuarios reales. Cuando se ejecuta la aplicación, COM+ aplicará la directiva mediante la realización de comprobaciones de roles.

Fundamentalmente, los roles ayudan a proteger el código, es decir, los métodos a los que pueden llamar los clientes de una aplicación COM+. La pertenencia a roles se comprueba cada vez que un cliente intenta llamar a un método expuesto por un componente en una aplicación. Si el autor de la llamada está en un rol asignado al método o recurso llamado, la llamada se realiza correctamente; de lo contrario, se produce un error.

## <a name="declarative-role-based-security"></a>Seguridad de Role-Based declarativa

Con la seguridad basada en roles declarativa, se declaran los roles administrativamente (mediante la herramienta administrativa Servicios de componentes o las funciones administrativas) y se asignan administrativamente a los recursos de la aplicación. Dónde y cómo se establece la seguridad declarativa determinará dónde se dibujan los límites de seguridad para la aplicación. Para obtener más información, vea [Límites de seguridad.](security-boundaries.md)

Puede asignar un rol determinado a toda la aplicación, a un componente determinado, a una interfaz determinada de un componente o a un método determinado en una interfaz. Las asignaciones de roles se heredan en la cadena natural de inclusión, es decir, si asigna un rol a un componente, se asigna implícitamente a cada interfaz y método expuestos por ese componente.

Con la disponibilidad de las asignaciones de roles de nivel de método, puede ayudar a proteger eficazmente los componentes e interfaces que no se han diseñado pensando en la seguridad. Sin embargo, si los propios métodos no son protegibles con asignaciones de roles declarativas, es posible que deba realizar la comprobación de roles mediante programación. Por lo general, es una buena idea tener en cuenta la seguridad a la hora de decidir cómo factorar la funcionalidad empresarial a través de métodos. De lo contrario, podría encontrarse agregando código relacionado con la seguridad en el último minuto.

Para obtener procedimientos detallados para establecer la seguridad basada en roles, vea [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Seguridad mediante programación

En algunas circunstancias, es posible que quiera colocar la lógica de seguridad en los componentes mientras sigue usando la seguridad basada en roles. Es posible que no se puedan tomar todas las decisiones de acceso a través de métodos, o no hacerlo. Por ejemplo, podría tener un recurso de aplicación privado, quizás una base de datos determinada, al que desea permitir que solo algunos autores de llamadas de un método accedan y excluyan otros. O bien, puede tener un único método TransferMoney y desea restringir algunos llamadores limitando la cantidad que pueden transferir.

En tales circunstancias, puede realizar la comprobación de roles en el código. Se proporciona una API sencilla que permite comprobar si la seguridad está activada y si un autor de la llamada o un usuario determinado tiene un rol determinado. Esta funcionalidad solo está disponible cuando está habilitada la seguridad basada en roles. Esto significa que todavía puede aprovechar la seguridad basada en roles declarativa cuando sea suficiente y, a continuación, puede ampliarla mediante programación a un nivel más preciso de granularidad cuando sea necesario.

Además, cuando se usa la seguridad basada en roles, se tiene acceso mediante programación a la información relativa a todos los autores de llamadas ascendentes en la cadena de llamadas al componente. Esto es especialmente útil cuando se quiere mantener un registro de auditoría detallado.

Para obtener descripciones de cómo realizar la comprobación de roles en el código y cómo acceder a la información de contexto de llamada de seguridad, vea [Seguridad de componentes mediante programación](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorización y autenticación

La autorización significativa presupone que está seguro de que los clientes son realmente quienes dicen ser. La comprobación de la identidad del cliente se controla por separado mediante un servicio de autenticación. Sin autenticación, básicamente permite que los llamadores entren en el sistema honor. Para obtener descripciones de la autenticación a medida que afecta a las aplicaciones COM+, vea [Autenticación de cliente](client-authentication.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño eficaz de roles](designing-roles-effectively.md)
</dt> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Propiedad de contexto de seguridad](security-context-property.md)
</dt> </dl>

 

 



