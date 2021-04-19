---
description: En muchos escenarios, la seguridad basada en roles es un mecanismo muy eficaz, pero hay situaciones en las que es menos eficaz.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Diseñar roles de forma eficaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a340cb2fc643a414ebf784a14e7b61a45bccd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538589"
---
# <a name="designing-roles-effectively"></a>Diseñar roles de forma eficaz

En muchos escenarios, la seguridad basada en roles es un mecanismo muy eficaz, pero hay situaciones en las que es menos eficaz. Debe tener en cuenta varios factores a la hora de decidir dónde y cómo aplicar la seguridad basada en roles a una aplicación determinada.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Características de usuario y datos y la idoneidad de los roles

Los roles funcionan muy bien para caracterizar a los grupos de usuarios y, en ese caso, filtran las acciones que pueden realizar esos usuarios. A menudo, esto se lleva a cabo en la práctica mediante la creación de roles que reflejan el lugar de un usuario dentro de una organización, por ejemplo, las funciones "administradores" y "cajeros", "administradores" y "lectores", "proyecto de un empleado" y "proyecto de dos empleados". En tales casos, en los que los datos a los que se tiene acceso son bastante genéricos con respecto a los usuarios, los roles se pueden usar de forma eficaz para aplicar reglas de negocios como las siguientes:

-   "Los administradores pueden transferir cualquier cantidad de dinero. Los cajeros solo pueden transferir hasta $10.000 ".

-   "Los administradores pueden cambiar cualquier cosa. Todos los demás solo pueden leer ".

-   "Project One Employees puede tener acceso a una determinada base de datos. Nadie más puede ".

Los usuarios pueden entrar en varios roles de forma natural, en función de cómo los roles modelan la estructura organizativa de una empresa.

Sin embargo, los roles no funcionan bien cuando una decisión de acceso de seguridad se sitúa en las características de un determinado dato. Por ejemplo, sería difícil utilizar roles para reflejar relaciones de datos de usuario complicadas, como las siguientes:

-   "Un administrador determinado solo puede acceder a los datos de personal de sus informes".

-   "El consumidor de Joe puede buscar el saldo de su cuenta".

En tales casos, la comprobación de seguridad se debe realizar a menudo en la base de datos, donde es más fácil tener en cuenta las características de INNATE de los datos a los que se tiene acceso. Esto significa que debe usar la *suplantación* para pasar la identidad del cliente a la base de datos y permitir que la base de datos valide la solicitud. Esto puede afectar al rendimiento y puede afectar al diseño de la aplicación; por ejemplo, la agrupación de conexiones podría no funcionar cuando se abre una conexión con una identidad de usuario determinada. Para obtener una explicación de los problemas implicados, consulte [seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md) y [delegación y delegación de clientes](client-impersonation-and-delegation.md).

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Complejidad y escalabilidad de una directiva de autorización de Role-Based

Cualquier directiva de seguridad que ponga en marcha solo será tan eficaz como su implementación por parte de los administradores del sistema que implementen la aplicación. Si los administradores cometen errores en la asignación de usuarios a los roles correctos según la Directiva de seguridad, la Directiva no funcionará según lo previsto. Es más probable que se produzcan problemas en las siguientes circunstancias:

-   Ha realizado una Directiva muy compleja basada en roles, con muchos roles y usuarios asignados a varios roles.
-   Los roles se crean con criterios ambiguos para los que deben pertenecer a ellos.
-   Hay muchos usuarios en el sitio donde se instala la aplicación y los usuarios se mueven con frecuencia dentro de la organización, cambiando con respecto a los roles que ha creado.
-   Hay muchos administradores en el sitio donde se instala la aplicación, con división de responsabilidades, de modo que un administrador familiarizado con los requisitos de seguridad de la aplicación no esté familiarizado con los grandes grupos de usuarios que deben usarlo. Este es un problema especial a medida que los usuarios se mueven dentro de la organización, por lo que la información debe comunicarse bien.

Además, a medida que aumenta el número de roles asignados a una aplicación, la cantidad de tiempo que COM+ debe invertir en buscar la pertenencia del llamador en esos roles, con una degradación probable del rendimiento.

Para administrar la complejidad y mitigar estos problemas, puede usar las siguientes directrices:

-   Elija nombres de rol que sean autodescriptivos. Haga que sea lo más obvio posible qué usuarios deben pertenecer a cada rol.
-   Haga que su directiva basada en roles sea lo más sencilla posible (y no más sencilla). Elija el menor número posible de roles, mientras mantiene una directiva efectiva.
-   Documente claramente la directiva basada en roles que crea para los administradores, si la pertenencia a roles es obvia (para usted). En concreto, use el campo de Descripción disponible para cada rol para describir la intención del rol. Si no puede describir generalmente quién debe pertenecer al rol en un par de oraciones, probablemente es demasiado complicado.
-   Recomendamos encarecidamente que los administradores de la aplicación rellenen los roles con grupos de usuarios en lugar de usuarios individuales. Se trata de una solución mucho más escalable. Facilita la reasignación o eliminación de usuarios a medida que se mueven dentro de la organización y aísla a los administradores de una determinada cantidad de supervisión y problemas de comunicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Propiedad de contexto de seguridad](security-context-property.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



