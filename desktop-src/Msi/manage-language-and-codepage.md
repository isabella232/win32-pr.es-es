---
description: El WiLangID.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Administrar idioma y página de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678402"
---
# <a name="manage-language-and-codepage"></a>Administrar idioma y página de códigos

El WiLangID.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se usa el script para tener acceso a la información de idioma y la página de códigos de un paquete. Para obtener más información, vea [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md) y [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md) del [ **objeto Database**](database-object.md)

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiLangID.vbs la \[ ruta de acceso al valor de la \] \[ palabra clave Database \] \[\]**

Especifique la ruta de acceso a la base de datos Windows Installer. Para cambiar un valor, especifique una de las siguientes palabras clave seguido del nuevo valor. Si no se especifica ningún valor, el ejemplo devuelve el valor actual.



| Palabra clave      | Descripción                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Package**  | Las versiones de idioma admitidas por la base de datos. Para obtener más información, consulte [**Template Summary**](template-summary.md) Property.                                                               |
| **Producto**  | Idioma que debe utilizar el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos. Para obtener más información, consulte propiedad [**ProductLanguage**](productlanguage.md) . |
| **Codepage** | Página de códigos ANSI única para el grupo de cadenas. Para obtener más información, vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).                                       |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). En el caso de utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

Para obtener más información, vea [determinar la página de códigos de una base](determining-an-installation-database-s-code-page.md) de datos de instalación y [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).

 

 



