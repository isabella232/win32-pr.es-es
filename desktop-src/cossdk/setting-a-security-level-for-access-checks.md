---
description: Una vez que haya habilitado las comprobaciones de acceso, para la aplicación COM+, debe seleccionar el nivel en el que desea que se realicen las comprobaciones de acceso.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Establecimiento de un nivel de seguridad para las comprobaciones de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153385"
---
# <a name="setting-a-security-level-for-access-checks"></a>Establecimiento de un nivel de seguridad para las comprobaciones de acceso

Una vez que haya habilitado las [comprobaciones de acceso](enabling-access-checks-for-an-application.md), para la aplicación com+, debe seleccionar el nivel en el que desea que se realicen las comprobaciones de acceso.

**Para seleccionar un nivel de seguridad**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación COM+ para la que desea habilitar las comprobaciones de acceso y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  En **nivel de seguridad**, seleccione una de las siguientes opciones:

    -   **Realizar comprobaciones de acceso solo en el nivel de proceso**: este valor indica que los usuarios de roles asignados a la aplicación se agregarán al descriptor de seguridad del proceso. Esto tiene los siguientes efectos e implicaciones:

        La comprobación de roles específica se desactiva en los niveles de componente, método y interfaz. Las comprobaciones de seguridad solo se realizan en el nivel de aplicación.

        La propiedad Security no se incluye en el contexto de los objetos que se ejecutan dentro de la aplicación. Esto puede afectar al modo en que se activan los objetos. Vea [propiedad de contexto de seguridad](security-context-property.md).

        El contexto de la llamada de seguridad no estará disponible. La seguridad mediante programación que se basa en la información de contexto de llamada de seguridad no funcionará. Vea [información sobre el contexto de llamada de seguridad](security-call-context-information.md).

    -   **Realizar comprobaciones de acceso en el nivel de proceso y de componente**: este valor indica que se realizarán comprobaciones de descriptores de seguridad de nivel de proceso y comprobaciones completas de seguridad basadas en roles. Esto tiene los siguientes efectos e implicaciones:

        Para habilitar la comprobación de roles para componentes concretos, debe [habilitar las comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md).

        La propiedad de seguridad se incluye en el contexto de los objetos que se ejecutan dentro de la aplicación. Esto puede afectar al modo en que se activan los objetos. Vea [propiedad de contexto de seguridad](security-context-property.md).

        El contexto de la llamada de seguridad está disponible. La seguridad basada en roles de programación está habilitada. Vea [información sobre el contexto de llamada de seguridad](security-call-context-information.md).

        > [!Note]  
        > En el caso de las aplicaciones de biblioteca COM+, debe elegir entre los niveles de componente en proceso y en los componentes para que funcionen todas las comprobaciones de acceso significativas. Las aplicaciones de biblioteca se basan en el proceso de host para la seguridad de nivel de proceso. Puede determinar cómo interactúa la aplicación de biblioteca con la autenticación realizada por el proceso de host mediante la configuración de la [autenticación](enabling-authentication-for-a-library-application.md). Para obtener más información, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).

         

4.  Haga clic en **OK**.

La próxima vez que se inicie la aplicación, la seguridad se comprobará automáticamente en el nivel especificado. Solo se concederá acceso a la aplicación a los usuarios asignados a los roles asignados a la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definición de roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitación de las comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



