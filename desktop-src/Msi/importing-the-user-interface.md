---
description: Además de la información que se describe en las secciones anteriores, uisample.msi también contiene datos para una interfaz de usuario de ejemplo.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importar el Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074425"
---
# <a name="importing-the-user-interface"></a>Importar el Interfaz de usuario

Además de la información que se describe en las secciones anteriores, uisample.msi también contiene datos para una interfaz de usuario de ejemplo. Si ha combinado uisample.msi en MNP2000.msi en la sección Importación de una base de datos en blanco [,](importing-a-blank-database.md)esta información también MNP2000.msi en blanco. La información de la interfaz de usuario de ejemplo se encuentra en las tablas siguientes.

-   [Tabla ActionText](actiontext-table.md)
-   [Tabla binaria](binary-table.md)
-   [Tabla de control](control-table.md)
-   [Tabla ControlEvent](controlevent-table.md)
-   [Tabla de diálogos](dialog-table.md)
-   [Tabla de errores](error-table.md)
-   [Tabla EventMapping](eventmapping-table.md)
-   [Tabla RadioButton](radiobutton-table.md)
-   [Tabla TextStyle](textstyle-table.md)
-   [TABLA UIText](uitext-table.md)

El editor de base de datos Orca proporcionado con el instalador incluye una opción de vista previa de diálogo que puede usar para obtener una vista previa de los diálogos de la interfaz de usuario especificados por los datos de las tablas anteriores.

El paquete de instalación de MNP2000.msi ya está listo para la validación del paquete. Ejecute siempre la validación en un nuevo paquete antes de intentar instalar el paquete por primera vez. Esto se describe en Validación del ejemplo de instalación.

Si no desea incluir la interfaz de usuario en el paquete de ejemplo, omita o quite toda la información de las tablas mostradas anteriormente, excepto la tabla [TextStyle](textstyle-table.md) (que es necesaria para definir la [**propiedad DefaultUIFont).**](defaultuifont.md) También debe quitar las propiedades de la interfaz de usuario de la [tabla de propiedades](property-table.md). A continuación se muestra una tabla de propiedades de ejemplo para Bloc de notas ejemplo, sin una interfaz de usuario. No reutilice los GUID que se muestran en la tabla si copia este ejemplo.

[Tabla de propiedades](property-table.md)



| Propiedad.                                   | Value                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**Fabricante**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 3082                                   |
| [**ProductName**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**UpgradeCode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

Un paquete sin una interfaz de usuario se puede instalar desde la línea de comandos o desde un programa. Para instalar un paquete desde la línea de comandos, use los métodos descritos en [Opciones de la línea de comandos](command-line-options.md). Para instalar un paquete desde un programa, use los métodos descritos en [Using Installer Functions](using-installer-functions.md). Ejecute siempre la validación en un nuevo paquete antes de intentar instalar un nuevo paquete por primera vez.

[Continuar](validating-an-installation-database.md)

 

 



