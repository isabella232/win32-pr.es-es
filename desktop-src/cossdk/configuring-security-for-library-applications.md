---
description: Hay consideraciones especiales a la hora de configurar la seguridad basada en roles y la autenticación para aplicaciones de biblioteca.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configuración de la seguridad para aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0d8b3993a00512c20409f1f029b7402d5f9ace97984cbe9757453b5672125f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548912"
---
# <a name="configuring-security-for-library-applications"></a>Configuración de la seguridad para aplicaciones de biblioteca

Hay consideraciones especiales a la hora de configurar la seguridad basada en roles y la autenticación para aplicaciones de biblioteca.

## <a name="enabling-or-disabling-authentication"></a>Habilitación o deshabilitación de la autenticación

Uno de los factores que se deben tener en cuenta es si los llamadores de la aplicación de biblioteca deben estar sujetos a las comprobaciones de seguridad de nivel de proceso del proceso de hospedaje, es decir, si se debe habilitar o deshabilitar la autenticación.

Por ejemplo, si la aplicación de biblioteca se hospedará en un explorador, es posible que tenga que recibir devoluciones de llamada no autenticadas. Para solucionar esta necesidad, puede deshabilitar la autenticación para que el proceso de hospedaje no realice comprobaciones de seguridad para los llamadores de la aplicación de biblioteca. Al deshabilitar la autenticación, la aplicación de biblioteca queda sin autenticar de forma eficaz: todas las llamadas a ella se completarán correctamente. Los llamadores de la aplicación de biblioteca no están sujetos a las comprobaciones de seguridad del proceso de hospedaje. Básicamente, la aplicación de biblioteca se etiqueta como "no autenticada" y se omiten las comprobaciones de seguridad para las llamadas a la aplicación de biblioteca.

Para obtener información sobre cómo habilitar o deshabilitar la autenticación, vea [Habilitar la autenticación para una aplicación de biblioteca.](enabling-authentication-for-a-library-application.md)

## <a name="enforcing-role-checks"></a>Aplicación de comprobaciones de roles

Otra decisión que se debe tomar es si la aplicación de biblioteca debe usar [la seguridad basada en roles](role-based-security-administration.md). Si se usa la seguridad basada en roles, debe usar la seguridad de nivel de componente para realizar las comprobaciones de acceso. Los roles asignados a la aplicación de biblioteca no se reflejan en el descriptor de seguridad del proceso. La única autorización que puede controlar la aplicación de biblioteca es en el nivel de componente. Para obtener más información sobre la seguridad de nivel de componente, vea [Límites de seguridad.](security-boundaries.md)

Para ver cómo establecer la seguridad de nivel de componente, vea [Establecer un nivel de seguridad para las comprobaciones de acceso.](setting-a-security-level-for-access-checks.md)

## <a name="configuration-scenarios"></a>Escenarios de configuración

Para comprender mejor las implicaciones de decidir si la aplicación de biblioteca debe usar la seguridad basada en roles y si la aplicación de biblioteca debe no estar autenticada, tenga en cuenta los siguientes escenarios:

-   **La autenticación está habilitada y se usa la seguridad basada en roles.** En este escenario, el proceso de hospedaje realiza comprobaciones de seguridad y a algunos llamadores se les deniega el acceso en el nivel de proceso. Además, la comprobación de roles se realiza en el nivel de aplicación de biblioteca para que a algunos llamadores que realizan la comprobación de seguridad de nivel de proceso se les deniegue el acceso a la aplicación de biblioteca cuando se comprueba la pertenencia a roles. Este es el escenario habitual para una aplicación de biblioteca COM+ que usa la seguridad basada en roles.

    En la ilustración siguiente se muestra el escenario en el que se habilita la autenticación y se usa la comprobación de roles.

    ![Diagrama que muestra la autenticación que tiene lugar dentro de un proceso de host.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **La autenticación está habilitada y no se usa la seguridad basada en roles.** En este escenario, las comprobaciones de seguridad se realizan en el nivel de proceso, pero la pertenencia a roles no se comprueba en el nivel de aplicación de biblioteca. Por lo tanto, a cualquier llamador de la aplicación de biblioteca que lo haga a través de la comprobación de seguridad de nivel de proceso se le dará acceso a la aplicación de biblioteca porque no se comprueba la pertenencia a roles. Esta situación existiría cuando se migra una aplicación COM que no usa la seguridad basada en roles a una aplicación de biblioteca COM+.

    En la ilustración siguiente se muestra el escenario en el que la autenticación está habilitada y no se está utilizando la comprobación de roles.

    ![Diagrama que muestra la autenticación de nivel de proceso para una aplicación de biblioteca dentro del proceso de host.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **La autenticación está deshabilitada y se usa la seguridad basada en roles.** En este escenario, las comprobaciones de seguridad se realizan en el nivel de proceso, pero los llamadores a la aplicación de biblioteca no están autenticados. En efecto, los llamadores de la aplicación de biblioteca están exentos de la comprobación de seguridad de nivel de proceso. Dado que la comprobación de roles está habilitada, la pertenencia a roles por sí sola determina quién tiene acceso a la aplicación de biblioteca. Este escenario podría ser adecuado cuando la comprobación de seguridad que realizaría el proceso de hospedaje es demasiado restrictiva, pero debe tener alguna restricción de acceso en la aplicación de biblioteca o en interfaces o métodos específicos. Este escenario le permite desactivar eficazmente la seguridad de los procesos y seguir teniendo comprobaciones de acceso de nivel adecuadas mediante la seguridad basada en roles.

    El escenario en el que la autenticación está deshabilitada y se está utilizando la comprobación de roles se muestra en la ilustración siguiente.

    ![Diagrama que muestra "comprobar la pertenencia a roles" en una aplicación de biblioteca dentro de un proceso de host.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **La autenticación está deshabilitada y no se usa la seguridad basada en roles.** En este escenario, las comprobaciones de seguridad se siguen haciendo en el nivel de proceso, pero, como en el escenario anterior, los llamadores de la aplicación de biblioteca siempre pasan esta comprobación de seguridad. Dado que la comprobación de roles también está deshabilitada, la pertenencia a roles no se comprueba en el nivel de aplicación de biblioteca. Básicamente, cualquier persona puede llamar a la aplicación de biblioteca. Este escenario debe elegirse cuando el objeto COM necesite recibir devoluciones de llamada no autenticadas, como podría ser el caso de un control ActiveX hospedado por Internet Explorer y con un complemento Microsoft Management Console. Por supuesto, este objeto COM debe ser de confianza para que se comporte correctamente al recibir llamadas no autenticadas. Por ejemplo, no debe tener acceso a archivos arbitrarios en nombre de sus llamadores.

    El escenario en el que la autenticación está deshabilitada y no se está utilizando la comprobación de roles se muestra en la ilustración siguiente.

    ![Diagrama que muestra las llamadas a una aplicación de biblioteca que no están autenticadas dentro del proceso de host.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Después de decidir si habilitar o deshabilitar la autenticación para la aplicación de biblioteca COM+, consulte Habilitación de la autenticación para una aplicación de biblioteca para obtener un procedimiento paso [a](enabling-authentication-for-a-library-application.md) paso que explica cómo deshabilitar (o habilitar) la autenticación mediante la herramienta administrativa Servicios de componentes. Si la aplicación de biblioteca va a usar la seguridad basada en roles, consulte [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de la aplicación de biblioteca](library-application-security.md)
</dt> </dl>

 

 



