---
description: Este ejemplo muestra cómo utilizar las acciones personalizadas para crear cuentas de usuario en un equipo local al instalar un componente.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Usar una acción personalizada para crear cuentas de usuario en un equipo local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360914"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Usar una acción personalizada para crear cuentas de usuario en un equipo local

Este ejemplo muestra cómo utilizar las acciones personalizadas para crear cuentas de usuario en un equipo local al instalar un componente. Al quitar un componente, se quitan las cuentas de usuario locales creadas por la acción personalizada. Se muestran varias acciones personalizadas, incluidas las acciones personalizadas de [ejecución aplazada](deferred-execution-custom-actions.md) y [las acciones personalizadas de reversión](rollback-custom-actions.md).

El ejemplo cumple las siguientes especificaciones.

-   La instalación de crea cuentas de usuario solo si se ejecuta Windows 2000.
-   La instalación de crea cuentas de usuario solo si el componente se está instalando para ejecutarse localmente. Esto evita la creación de cuentas de usuario durante la reparación o reinstalación del componente.
-   El instalador quita las cuentas cuando se quita el componente.
-   La información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no está codificada de forma rígida en el código de acción personalizada.
-   Dado que la creación o eliminación de cuentas de usuario requiere privilegios elevados, algunas de las acciones personalizadas deben ser capaces de realizar cambios en el sistema que requieran privilegios elevados. Estas acciones personalizadas deben ser acciones personalizadas diferidas que se ejecutan en el script de ejecución.
-   Cada cuenta tiene una acción personalizada de reversión para asegurarse de que la cuenta se quita al revertir la instalación del componente. Esto no incluye la reversión de la eliminación de una cuenta durante la eliminación de un componente.
-   Las acciones personalizadas envían mensajes ActionData para cada cuenta que se crea o se quita. Esto no incluye el suministro de mensajes de progreso para ProgressBar.
-   Las acciones personalizadas notifican un error si no se puede crear una cuenta.
-   La contraseña de la cuenta se obtiene a través de la interacción del usuario con la interfaz de usuario o, en el caso de una instalación en la interfaz de usuario básica o en ningún [nivel de interfaz de usuario](user-interface-levels.md), como una propiedad pasada en la línea de comandos.
-   Los datos confidenciales se ocultan del archivo de registro.

El ejemplo incluye un componente hipotético denominado TestAccount. En la explicación de las secciones siguientes se supone que ya ha creado los recursos necesarios para TestAccount y que ha creado la [característica](feature-table.md), el [componente](component-table.md), el [archivo](file-table.md), el [directorio](directory-table.md)y las tablas de [FeatureComponents](featurecomponents-table.md) en la base de datos de ejemplo necesaria para instalar este componente. Para obtener más información, vea [un ejemplo de instalación](an-installation-example.md).

Los temas siguientes contienen información acerca de cómo crear las acciones personalizadas necesarias y agregarlas a un paquete de instalación.

-   [Crear las acciones personalizadas](authoring-the-custom-actions.md)
-   [Agregar una tabla CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md)
-   [Creación de la tabla CustomAction](authoring-the-customaction-table.md)
-   [Creación de las tablas de error y de ActionText](authoring-the-actiontext-and-error-tables.md)
-   [Crear la tabla InstallExecuteSequence](authoring-the-installexecutesequence-table.md)
-   [Crear la interfaz de usuario para la entrada de contraseña](authoring-the-user-interface-for-password-input.md)
-   [Protección de la instalación](securing-the-installation.md)

 

 



