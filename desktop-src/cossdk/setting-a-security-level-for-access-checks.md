---
description: Después de habilitar las comprobaciones de acceso, para la aplicación COM+, debe seleccionar el nivel en el que desea que se realicen las comprobaciones de acceso.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Establecer un nivel de seguridad para las comprobaciones de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e912f671a27d35b51939376fa14af3b693c368e3375680913693d364ddf638
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120375"
---
# <a name="setting-a-security-level-for-access-checks"></a>Establecer un nivel de seguridad para las comprobaciones de acceso

Después de habilitar [las comprobaciones de](enabling-access-checks-for-an-application.md)acceso, para la aplicación COM+, debe seleccionar el nivel en el que desea que se realicen comprobaciones de acceso.

**Para seleccionar un nivel de seguridad**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en la aplicación COM+ para la que desea habilitar las comprobaciones de acceso y, a continuación, haga clic **en Propiedades**.

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad .

3.  En **Nivel de seguridad,** seleccione una de las siguientes opciones:

    -   **Realizar comprobaciones de acceso** solo en el nivel de proceso: esta configuración indica que los usuarios de roles asignados a la aplicación se agregarán al descriptor de seguridad del proceso. Esto tiene los siguientes efectos e implicaciones:

        La comprobación de roles detallada está desactivada en los niveles de componente, método e interfaz. Las comprobaciones de seguridad solo se realizan en el nivel de aplicación.

        La propiedad de seguridad no se incluye en el contexto de los objetos que se ejecutan dentro de la aplicación. Esto puede afectar potencialmente a cómo se activan los objetos. Vea [Propiedad de contexto de seguridad](security-context-property.md).

        El contexto de llamada de seguridad no estará disponible. La seguridad mediante programación que se basa en la información de contexto de llamada de seguridad no funcionará. Vea Información [de contexto de llamada de seguridad](security-call-context-information.md).

    -   **Realizar comprobaciones de acceso en** el nivel de proceso y componente: esta configuración indica que se realizarán comprobaciones del descriptor de seguridad de nivel de proceso y comprobaciones de seguridad basadas en roles completa. Esto tiene los siguientes efectos e implicaciones:

        Para habilitar la comprobación de roles para componentes concretos, debe habilitar [las comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md).

        La propiedad de seguridad se incluye en el contexto de los objetos que se ejecutan dentro de la aplicación. Esto puede afectar potencialmente a cómo se activan los objetos. Vea [Propiedad de contexto de seguridad](security-context-property.md).

        El contexto de llamada de seguridad está disponible. La seguridad basada en roles mediante programación está habilitada. Vea Información [de contexto de llamada de seguridad](security-call-context-information.md).

        > [!Note]  
        > En el caso de las aplicaciones de biblioteca COM+, debe elegir comprobar tanto en el proceso como en los niveles de componente para que funcione cualquier comprobación de acceso significativa. Las aplicaciones de biblioteca se basan en el proceso de host para la seguridad de nivel de proceso. Puede determinar cómo interactúa la aplicación de biblioteca con la autenticación realizada por el proceso de host [estableciendo la autenticación](enabling-authentication-for-a-library-application.md). Para obtener más información, vea [Library Application Security](library-application-security.md).

         

4.  Haga clic en **Aceptar**.

La próxima vez que se inicie la aplicación, la seguridad se comprobará automáticamente en el nivel especificado. Solo los usuarios asignados a roles asignados a la aplicación tendrán acceso a la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Definir roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



