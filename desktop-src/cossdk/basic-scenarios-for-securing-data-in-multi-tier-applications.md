---
description: En este tema se presentan algunos escenarios de bloques de creación, que ilustran los criterios que se describen en decidir dónde aplicar la seguridad.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Escenarios básicos para la protección de datos en aplicaciones de niveles múltiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705335"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Escenarios básicos para la protección de datos en aplicaciones de niveles múltiples

En este tema se presentan algunos escenarios de bloques de creación, que ilustran los criterios [que se describen en decidir dónde aplicar la seguridad](deciding-where-to-enforce-security.md).

## <a name="trusted-server-scenario"></a>Escenario de servidor de confianza

-   La base de datos confía totalmente en la aplicación COM+ para autenticar y autorizar a los usuarios finales para que tengan acceso a los datos de la base de datos.
-   Preferiblemente, la base de datos está protegida contra cualquier acceso excepto a través de la aplicación.
-   La aplicación COM+ utiliza la seguridad basada en roles para autorizar a los usuarios.
-   Las conexiones se abren en la identidad de la aplicación COM+ y se pueden agrupar por completo.
-   La aplicación COM+ puede realizar la auditoría y el registro, o la aplicación puede pasar esta información a la base de datos.

Este escenario funciona mejor con los datos a los que se puede tener acceso mediante categorías de usuarios predecibles que se pueden encapsular en roles. Por ejemplo, solo los "administradores", "cajeros" y "contables" tienen permiso para acceder a las cuentas. La lógica de negocios de lo que se habilita para cada una de ellas se aplica en el nivel intermedio.

## <a name="impersonation-scenario"></a>Escenario de suplantación

-   La base de datos realiza su propia autenticación y autorización de los usuarios finales para ayudar a limitar el acceso a los datos de la base de datos.
-   La aplicación COM+ suplanta a los clientes cada vez que accede a la base de datos.
-   Las conexiones se realizan en cada llamada y no se pueden volver a usar.

Este escenario funciona mejor con los datos que están estrechamente enlazados a las clases de usuarios muy pequeñas. Por ejemplo, cada empleado puede tener acceso únicamente a su propio archivo de personal, y cada administrador solo puede tener acceso a los archivos de personal de sus informes.

## <a name="hybrid-scenario"></a>Escenario híbrido

Una combinación de los dos escenarios anteriores, donde la suplantación solo se utiliza cuando es necesario.

Este escenario funciona mejor en situaciones en las que tiene relaciones de datos de usuario híbridos. Por ejemplo, tiene "administradores", "cajeros", "contables" y miles de clientes Web individuales que pueden tener acceso a solo sus propias cuentas. Puede separar las rutas de acceso lógicas a través de la aplicación, potencialmente con componentes independientes, para administrar la última clase de usuarios, especialmente cuando las suposiciones de rendimiento para esos usuarios son diferentes.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Escenario de confianza con roles de Microsoft SQL Server

-   Microsoft SQL Server 7,0 y versiones posteriores pueden autorizar el acceso a filas específicas mediante roles, pero confía en la aplicación COM+ para autenticar y autorizar a los usuarios y asignarlos a los roles correctos en la base de datos.
-   La aplicación COM+ autoriza a los usuarios mediante la seguridad basada en roles y los roles de aplicación se corresponden bien con los roles de base de datos.
-   Se pueden abrir conexiones que son específicas de un rol de base de datos determinado. Estas conexiones se pueden reutilizar si están retenidas por objetos agrupados en las aplicaciones COM+. Para obtener más información sobre cómo hacerlo, consulte [agrupación de objetos com+](com--object-pooling.md).
-   La aplicación COM+ puede realizar la auditoría y el registro, o la aplicación puede pasar esta información a la base de datos.

Este escenario funciona mejor por lo general en los mismos tipos de usuarios y datos que en el primer escenario de servidor de confianza, ya que la aplicación COM+ sigue siendo de confianza para administrar correctamente la autorización. Sin embargo, protege la base de datos frente al acceso no autorizado, a la vez que permite el acceso desde varios orígenes externos a la aplicación COM+, sin incurrir en las penalizaciones de escala y rendimiento presentes en el escenario de suplantación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Decidir dónde aplicar la seguridad](deciding-where-to-enforce-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> </dl>

 

 



