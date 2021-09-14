---
description: En muchos escenarios, la seguridad basada en roles es un mecanismo muy eficaz, pero hay situaciones en las que es menos eficaz.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Diseño eficaz de roles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a340cb2fc643a414ebf784a14e7b61a45bccd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240891"
---
# <a name="designing-roles-effectively"></a>Diseño eficaz de roles

En muchos escenarios, la seguridad basada en roles es un mecanismo muy eficaz, pero hay situaciones en las que es menos eficaz. Debe tener en cuenta una serie de factores a la hora de decidir dónde y cómo aplicar la seguridad basada en roles a una aplicación determinada.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Características de usuario y datos y idoneidad de roles

Los roles funcionan muy bien para caracterizar grupos de usuarios y, en ese caso, filtrar qué acciones pueden realizar esos usuarios. A menudo, esto se lleva a cabo en la práctica mediante la creación de roles que reflejan el lugar de un usuario dentro de una organización, por ejemplo, los roles "Managers" y "Tellers", "Administrators" y "Readers", "Project One Employees" y "Project Two Employees". En tales casos, cuando los datos a los que se accede es bastante genérico con respecto a los usuarios, los roles se pueden usar de forma eficaz para aplicar reglas de negocios como las siguientes:

-   "Los administradores pueden transferir cualquier cantidad de dinero. Los tellers solo pueden transferir hasta 10 000 USD".

-   "Los administradores pueden cambiar cualquier cosa. Todos los demás solo pueden leer".

-   "Project un empleado puede acceder a una base de datos determinada. Nadie más puede".

Los usuarios pueden entrar de forma natural en varios roles, dependiendo de cómo modelen los roles la estructura organizativa de una empresa.

Sin embargo, los roles no funcionan muy bien cuando una decisión de acceso de seguridad depende de las características de un determinado fragmento de datos. Por ejemplo, sería difícil usar roles para reflejar relaciones complicadas entre usuario y datos, como las siguientes:

-   "Un administrador determinado puede acceder a los datos del personal solo para sus informes".

-   "Joe Consumer puede buscar el saldo de su cuenta".

En tales casos, la comprobación de seguridad se debe realizar a menudo en la propia base de datos, donde es más fácil tener en cuenta las características innate de los datos a los que se accede. Esto significa que debe usar la *suplantación para* pasar la identidad de cliente a la base de datos y permitir que la base de datos valide la solicitud. Esto puede afectar al rendimiento y puede afectar al diseño de la aplicación; por ejemplo, es posible que la agrupación de conexiones no funcione cuando se abre una conexión bajo una identidad de usuario determinada. Para obtener una explicación de los problemas implicados, [vea Seguridad de](multi-tier-application-security.md) aplicaciones de niveles múltiples y [Suplantación](client-impersonation-and-delegation.md)y delegación de cliente.

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Complejidad y escalabilidad de una directiva de Role-Based autorización

Cualquier directiva de seguridad que haya puesto en marcha solo será tan eficaz como su implementación por parte de los administradores del sistema que implemente la aplicación. Si los administradores cometen errores al asignar usuarios a los roles correctos según la directiva de seguridad, la directiva no funcionará según lo previsto. Es más probable que se produzcan problemas en las siguientes circunstancias:

-   Ha realizado una directiva muy compleja basada en roles, con muchos roles y usuarios asignando a numerosos roles.
-   Puede crear roles con criterios ambiguos para quién debe pertenecer a ellos.
-   Hay muchos usuarios en el sitio donde está instalada la aplicación y los usuarios se mueven con frecuencia dentro de la organización, cambiando con respecto a los roles que ha creado.
-   Hay muchos administradores en el sitio donde está instalada la aplicación, con división de responsabilidades, para que un administrador familiarizado con los requisitos de seguridad de la aplicación no esté familiarizado con los grandes grupos de usuarios que deben usarla. Esto es especialmente importante, ya que los usuarios se mueven dentro de la organización; esta información debe estar bien comunicada.

Además, a medida que aumenta el número de roles asignados a una aplicación, también aumenta la cantidad de tiempo que COM+ debe dedicar a buscar la pertenencia al llamador en esos roles, con una degradación probable del rendimiento.

Para administrar la complejidad y mitigar estos problemas, puede usar las siguientes directrices:

-   Elija nombres de rol autodescriptibles. Haga que sea lo más obvio posible qué usuarios deben pertenecer a qué roles.
-   Haga que la directiva basada en roles sea lo más sencilla posible (y que no sea más sencilla). Elija el menor número de roles posible, al tiempo que mantiene una directiva eficaz.
-   Documente claramente la directiva basada en roles que crea para los administradores, si la pertenencia a roles es obvia (para usted). En concreto, use el campo de descripción disponible para cada rol para describir la intención del rol. Si no se puede describir con carácter general quién debe pertenecer al rol en un par de oraciones, probablemente sea demasiado complicado.
-   Se recomienda encarecidamente que los administradores de la aplicación rellenen los roles con grupos de usuarios en lugar de usuarios individuales. Se trata de una solución mucho más escalable. Facilita la reasignación o eliminación de usuarios a medida que se mueven dentro de la organización y aísla a los administradores de una cierta cantidad de supervisión y problemas en la comunicación.

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

 

 



