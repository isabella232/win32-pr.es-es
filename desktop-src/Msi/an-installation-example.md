---
description: En este ejemplo se muestra cómo crear un paquete Windows Installer que instala una aplicación.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Ejemplo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159138"
---
# <a name="an-installation-example"></a>Ejemplo de instalación

En este ejemplo se muestra cómo crear un paquete Windows Installer que instala una aplicación. El ejemplo instala Bloc de notas, un editor de texto incluido con Windows y varios archivos de texto que describen eventos e admisiones en el imaginario Red Park Campos.

El ejemplo tiene las especificaciones siguientes:

-   La aplicación se proporciona a los usuarios como un paquete de Windows Installer que instala todos los archivos, accesos directos e información del Registro necesarios.
-   El paquete de instalación puede presentar un asistente de interfaz de usuario al usuario durante la instalación para recopilar información del usuario.
-   Durante la instalación, los usuarios tienen la opción de seleccionar características individuales que se instalarán para ejecutarse localmente, ejecutarse desde el origen o no instalarse.
-   Una de las características se puede presentar a los usuarios como una característica de instalación a petición.
-   El mismo paquete desinstala la aplicación y quita todos los archivos de aplicación y la información del Registro del equipo del usuario.
-   El paquete está preparado para recibir una actualización importante que incluye el cambio de su código de producto.

Para reproducir el ejemplo, necesita una herramienta de software capaz de crear y editar una base de datos en blanco Windows instalador. Hay varias herramientas de creación de paquetes disponibles de proveedores de software independientes. Se Windows editor de base de datos del instalador de Windows llamado Orca en Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Para completar el ejemplo, siga estos pasos:

[Planear la instalación](planning-the-installation.md)

[Importar una base de datos en blanco](importing-a-blank-database.md)

[Especificar la estructura de directorios](specifying-directory-structure.md)

[Especificar componentes](specifying-components.md)

[Especificar archivos y atributos de archivo](specifying-files-and-file-attributes.md)

[Especificar medios de origen](specifying-source-media.md)

[Especificar características](specifying-features.md)

[Especificar relaciones Feature-Component datos](specifying-feature-component-relationships.md)

[Agregar información del Registro](adding-registry-information.md)

[Especificar accesos directos](specifying-shortcuts.md)

[Especificar propiedades](specifying-properties.md)

[Importación de InstallExecuteSequence](importing-the-installexecutesequence.md)

[Importación de InstallUISequence](importing-the-installuisequence.md)

[Importación de AdminExecuteSequence](importing-the-adminexecutesequence.md)

[Importación de AdminUISequence](importing-the-adminuisequence.md)

[Importación de AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[Agregar información de resumen](adding-summary-information.md)

[Importar el Interfaz de usuario](importing-the-user-interface.md)

[Validar una base de datos de instalación](validating-an-installation-database.md)

 

 



