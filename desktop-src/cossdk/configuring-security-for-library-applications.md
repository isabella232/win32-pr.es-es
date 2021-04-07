---
description: Hay algunas consideraciones especiales para configurar la seguridad basada en roles y la autenticación para las aplicaciones de biblioteca.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configuración de la seguridad para aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102d6a0f102bfd19da0073bca14df8a8211203b1
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104003270"
---
# <a name="configuring-security-for-library-applications"></a>Configuración de la seguridad para aplicaciones de biblioteca

Hay algunas consideraciones especiales para configurar la seguridad basada en roles y la autenticación para las aplicaciones de biblioteca.

## <a name="enabling-or-disabling-authentication"></a>Habilitación o deshabilitación de la autenticación

Uno de los factores a tener en cuenta es si los autores de la llamada de la aplicación de biblioteca deben estar sujetos a las comprobaciones de seguridad de nivel de proceso del proceso de hospedaje, es decir, si se debe habilitar o deshabilitar la autenticación.

Por ejemplo, si un explorador hospeda la aplicación de biblioteca, es posible que necesite recibir devoluciones de llamada no autenticadas. Para satisfacer esta necesidad, puede deshabilitar la autenticación para que el proceso de hospedaje no realice comprobaciones de seguridad para los llamadores de la aplicación de biblioteca. Al deshabilitar la autenticación, la aplicación de biblioteca se queda sin autenticar, todas las llamadas a ella se realizarán correctamente. Los autores de llamadas de la aplicación de biblioteca no están sujetos a las comprobaciones de seguridad del proceso de hospedaje. Básicamente, la aplicación de biblioteca se etiqueta como "no autenticada" y se omiten las comprobaciones de seguridad para las llamadas a la aplicación de biblioteca.

Para obtener información acerca de cómo habilitar o deshabilitar la autenticación, consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md).

## <a name="enforcing-role-checks"></a>Aplicar comprobaciones de rol

Otra decisión que tomar es si la aplicación de biblioteca debe utilizar la [seguridad basada en roles](role-based-security-administration.md). Si se utiliza la seguridad basada en roles, debe utilizar la seguridad de nivel de componente para cualquier comprobación de acceso que se lleve a cabo. Los roles asignados a la aplicación de biblioteca no se reflejan en el descriptor de seguridad del proceso. La única autorización que puede controlar la aplicación de biblioteca es en el nivel de componente. Para obtener más información sobre la seguridad de nivel de componente, vea [límites de seguridad](security-boundaries.md).

Para ver cómo establecer la seguridad de nivel de componente, consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Escenarios de configuración

Para comprender mejor las implicaciones de decidir si la aplicación de biblioteca debe utilizar la seguridad basada en roles y si la aplicación de biblioteca debe estar sin autenticar, tenga en cuenta los siguientes escenarios:

-   **La autenticación está habilitada y se usa la seguridad basada en roles.** En este escenario, el proceso de hospedaje realiza comprobaciones de seguridad y a algunos llamadores se les deniega el acceso en el nivel de proceso. Además, la comprobación de roles se realiza en el nivel de aplicación de biblioteca, de modo que algunos autores de llamadas que lo hacen a través de la comprobación de seguridad de nivel de proceso se les deniega el acceso a la aplicación de biblioteca cuando se comprueba la pertenencia al rol. Este es el escenario habitual para una aplicación de biblioteca COM+ que utiliza la seguridad basada en roles.

    En la siguiente ilustración se muestra el escenario en el que la autenticación está habilitada y se usa la comprobación de roles.

    ![Diagrama que muestra la autenticación que tiene lugar dentro de un proceso de host.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **La autenticación está habilitada y no se utiliza la seguridad basada en roles.** En este escenario, las comprobaciones de seguridad se realizan en el nivel de proceso, pero la pertenencia a roles no se comprueba en el nivel de aplicación de biblioteca. Por lo tanto, cualquier llamador de la aplicación de biblioteca que lo hace a través de la comprobación de seguridad de nivel de proceso recibirá acceso a la aplicación de biblioteca porque no se comprueba la pertenencia a roles. Esta situación existe cuando una aplicación COM que no utiliza la seguridad basada en roles se migra a una aplicación de biblioteca COM+.

    En la siguiente ilustración se muestra el escenario en el que la autenticación está habilitada y no se está usando la comprobación de roles.

    ![Diagrama que muestra la autenticación de nivel de proceso para una aplicación de biblioteca dentro del proceso de host.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **La autenticación está deshabilitada y se usa la seguridad basada en roles.** En este escenario, las comprobaciones de seguridad se realizan en el nivel de proceso, pero los llamadores a la aplicación de biblioteca no se autentican. En efecto, los autores de la llamada de la aplicación de biblioteca están exentos de la comprobación de seguridad de nivel de proceso. Dado que la comprobación de roles está habilitada, la pertenencia a roles solo determina quién tiene acceso a la aplicación de biblioteca. Este escenario puede ser adecuado cuando la comprobación de seguridad que se realizaría en el proceso de hospedaje es demasiado restrictiva, pero debe tener alguna restricción de acceso en la aplicación de biblioteca o en interfaces o métodos específicos. Este escenario permite desactivar la seguridad del proceso de forma eficaz y seguir teniendo las comprobaciones de acceso de nivel adecuadas mediante la seguridad basada en roles.

    En la siguiente ilustración se muestra el escenario en el que la autenticación está deshabilitada y la comprobación de roles se está usando.

    ![Diagrama que muestra la "comprobación de la pertenencia a roles" en una aplicación de biblioteca dentro de un proceso de host.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **La autenticación está deshabilitada y no se utiliza la seguridad basada en roles.** En este escenario, las comprobaciones de seguridad se siguen realizando en el nivel de proceso, pero, como en el escenario anterior, los llamadores de la aplicación de biblioteca siempre pasan esta comprobación de seguridad. Dado que la comprobación de roles también está deshabilitada, la pertenencia a roles no se comprueba en el nivel de aplicación de biblioteca. Esencialmente, cualquier usuario puede llamar a la aplicación de biblioteca. Este escenario debe elegirse cuando el objeto COM necesite recibir devoluciones de llamada no autenticadas, como podría ser el caso de un control ActiveX hospedado por Internet Explorer y con un complemento de Microsoft Management Console. Por supuesto, este objeto COM debe ser de confianza para que se comporte de forma adecuada al recibir llamadas no autenticadas. Por ejemplo, no debería tener acceso a archivos arbitrarios en nombre de sus llamadores.

    En la siguiente ilustración se muestra el escenario en el que la autenticación está deshabilitada y la comprobación de roles no se está usando.

    ![Diagrama que muestra las llamadas a una aplicación de biblioteca que no se autentican en el proceso de host.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Una vez que haya decidido habilitar o deshabilitar la autenticación para la aplicación de biblioteca COM+, consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md) para obtener un procedimiento paso a paso que explica cómo deshabilitar o habilitar la autenticación mediante la herramienta administrativa Servicios de componentes. Si la aplicación de biblioteca va a utilizar la seguridad basada en roles, consulte Configuración de la [seguridad de Role-Based](configuring-role-based-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> </dl>

 

 



