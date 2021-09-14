---
description: En este tema se presentan algunos escenarios de bloque de creación, que ilustran los criterios que se deban analizar en Decisión de dónde aplicar la seguridad.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Escenarios básicos para proteger datos en aplicaciones de niveles múltiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073013"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Escenarios básicos para proteger datos en aplicaciones de niveles múltiples

En este tema se presentan algunos escenarios de bloque de creación, en los que se ilustran los criterios que se deban analizar [en Decidir dónde aplicar la seguridad.](deciding-where-to-enforce-security.md)

## <a name="trusted-server-scenario"></a>Escenario de servidor de confianza

-   La base de datos confía plenamente en la aplicación COM+ para autenticar y autorizar a los usuarios finales a acceder a los datos de la base de datos.
-   Preferiblemente, la base de datos está protegida contra cualquier acceso, excepto a través de la aplicación.
-   La aplicación COM+ usa la seguridad basada en roles para autorizar a los usuarios.
-   Las conexiones se abren bajo la identidad de la aplicación COM+ y son totalmente agrupables.
-   La aplicación COM+ puede realizar la auditoría y el registro, o la aplicación puede pasar esta información a la base de datos.

Este escenario funciona mejor para los datos a los que se puede acceder mediante categorías predecibles de usuarios que se pueden encapsular en roles. Por ejemplo, solo "Managers", "Tellers" y "Accountants" tienen permiso para acceder a las cuentas. La lógica de negocios de lo que está habilitado para hacer cada uno de ellos se aplica en el nivel intermedio.

## <a name="impersonation-scenario"></a>Escenario de suplantación

-   La base de datos realiza su propia autenticación y autorización de los usuarios finales para ayudar a limitar el acceso a los datos de la base de datos.
-   La aplicación COM+ suplanta a los clientes cada vez que accede a la base de datos.
-   Las conexiones se realizan por llamada y no se pueden reutilizar.

Este escenario funciona mejor para los datos estrechamente enlazados a clases muy pequeñas de usuarios. Por ejemplo, cada empleado solo puede acceder a su propio archivo de personal y cada administrador solo puede acceder a los archivos de personal de sus informes.

## <a name="hybrid-scenario"></a>Escenario híbrido

Combinación de los dos escenarios anteriores, donde la suplantación solo se usa cuando es necesaria.

Este escenario funciona mejor en situaciones en las que tiene relaciones híbridas entre usuario y datos. Por ejemplo, tiene "Managers", "Tellers", "Accountants" y miles de clientes web individuales que pueden acceder solo a sus propias cuentas. Puede separar las rutas de acceso lógicas a través de la aplicación, potencialmente con componentes independientes, para controlar la última clase de usuarios, especialmente donde las suposiciones de rendimiento para esos usuarios son diferentes.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Escenario de confianza mediante Microsoft SQL Server roles

-   Microsoft SQL Server 7.0 y versiones posteriores pueden autorizar el acceso a filas específicas mediante roles, pero confía en la aplicación COM+ para autenticar y autorizar a los usuarios y asignarlos a los roles correctos en la base de datos.
-   La aplicación COM+ autoriza a los usuarios mediante la seguridad basada en roles y los roles de aplicación se corresponden bien con los roles de base de datos.
-   Se pueden abrir conexiones específicas de un rol de base de datos determinado. Estas conexiones se pueden reutilizar si las mantienen objetos agrupados en las aplicaciones COM+. Para obtener más información sobre cómo hacerlo, vea [Agrupación de objetos COM+.](com--object-pooling.md)
-   La aplicación COM+ puede realizar la auditoría y el registro, o la aplicación puede pasar esta información a la base de datos.

Este escenario funciona mejor por lo general con los mismos tipos de usuarios y datos que en el primer escenario de servidor de confianza, ya que la aplicación COM+ sigue siendo de confianza para controlar correctamente la autorización. Sin embargo, ayuda a proteger la base de datos contra el acceso no autorizado, al tiempo que permite el acceso potencialmente desde varios orígenes fuera de la aplicación COM+, sin incurrir en las penalizaciones de escalado y rendimiento presentes en el escenario de suplantación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Decidir dónde aplicar la seguridad](deciding-where-to-enforce-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> </dl>

 

 



