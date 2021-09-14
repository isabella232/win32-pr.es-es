---
description: El archivo VBScript WiLangID.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Administrar lenguaje y página de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071922"
---
# <a name="manage-language-and-codepage"></a>Administrar lenguaje y página de códigos

El archivo vbscript WiLangID.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo se usa el script para acceder a la información de idioma y a la página de códigos de un paquete. Para obtener más información, vea [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and Code Page Handling (Windows Installer) [Localizing a Windows Installer Package and [Code Page Handling (Windows Installer]).](code-page-handling-windows-installer-.md)

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md) del objeto [ **Database**](database-object.md)

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiLangID.vbs cscript \[ al valor de palabra clave de base de \] \[ \] \[ datos\]**

Especifique la ruta de acceso a la base Windows del instalador. Para cambiar un valor, especifique una de las siguientes palabras clave seguida del nuevo valor. Si no se especifica ningún valor, el ejemplo devuelve el valor actual.



| Palabra clave      | Descripción                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Paquete**  | Las versiones de idioma admitidas por la base de datos. Para obtener información, consulte [**La propiedad Resumen de**](template-summary.md) plantilla.                                                               |
| **Producto**  | Idioma que el instalador debe usar para cualquier cadena de la interfaz de usuario que no se cree en la base de datos. Para obtener información, vea [**Propiedad ProductLanguage.**](productlanguage.md) |
| **Codepage** | Página de códigos ANSI única para el grupo de cadenas. Para obtener información, vea [Control de páginas de códigos (Windows Installer).](code-page-handling-windows-installer-.md)                                       |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

Para obtener más información, vea [Determinar la página](determining-an-installation-database-s-code-page.md) de códigos de una base de datos de instalación y Establecer la página de códigos de una base de [datos](setting-the-code-page-of-a-database.md).

 

 



