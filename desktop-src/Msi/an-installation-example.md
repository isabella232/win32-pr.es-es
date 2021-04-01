---
description: En este ejemplo se muestra cómo crear un paquete de Windows Installer simple que instala una aplicación.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Un ejemplo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909110"
---
# <a name="an-installation-example"></a>Un ejemplo de instalación

En este ejemplo se muestra cómo crear un paquete de Windows Installer simple que instala una aplicación. En el ejemplo se instala el Bloc de notas, un editor de texto incluido en Windows y varios archivos de texto que describen eventos y admisiones en el ámbito de estacionamiento rojo imaginario.

El ejemplo tiene las siguientes especificaciones:

-   La aplicación se proporciona a los usuarios como un paquete de Windows Installer de instalación automática que instala todos los archivos necesarios, accesos directos e información del registro.
-   El paquete de instalación puede presentar al usuario un asistente para la interfaz de usuario durante la instalación para recopilar información del usuario.
-   Durante la instalación, los usuarios tienen la opción de seleccionar las características individuales que se instalarán para ejecutarse: localmente, en ejecutar desde el origen o en no instalarse.
-   Una de las características se puede presentar a los usuarios como una característica de instalación a petición.
-   El mismo paquete desinstala la aplicación y quita todos los archivos de aplicación y la información del registro del equipo del usuario.
-   El paquete está preparado para recibir una actualización importante que incluye el cambio de su código de producto.

Para reproducir el ejemplo, necesita una herramienta de software capaz de crear y editar una base de datos Windows Installer en blanco. Hay varias herramientas de creación de paquetes disponibles de fabricantes de software independientes. En los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md)se proporciona un editor de base de datos de Windows Installer denominado orca.

Para completar el ejemplo, siga estos pasos:

[Planeación de la instalación](planning-the-installation.md)

[Importar una base de datos en blanco](importing-a-blank-database.md)

[Especificar la estructura de directorios](specifying-directory-structure.md)

[Especificar componentes](specifying-components.md)

[Especificar archivos y atributos de archivo](specifying-files-and-file-attributes.md)

[Especificar medios de origen](specifying-source-media.md)

[Especificar características](specifying-features.md)

[Especificar relaciones Feature-Component](specifying-feature-component-relationships.md)

[Agregar información del registro](adding-registry-information.md)

[Especificar accesos directos](specifying-shortcuts.md)

[Especificar propiedades](specifying-properties.md)

[Importación de InstallExecuteSequence](importing-the-installexecutesequence.md)

[Importación de InstallUISequence](importing-the-installuisequence.md)

[Importación de AdminExecuteSequence](importing-the-adminexecutesequence.md)

[Importación de AdminUISequence](importing-the-adminuisequence.md)

[Importación de AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[Agregar información de Resumen](adding-summary-information.md)

[Importación de la interfaz de usuario](importing-the-user-interface.md)

[Validar una base de datos de instalación](validating-an-installation-database.md)

 

 



