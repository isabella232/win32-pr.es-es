---
description: El WiSumInf.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo se puede usar para administrar la secuencia de información de Resumen de un paquete de Windows Installer.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Administrar información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ff360bd56dabc57b3a7ffccdba8c4f90346193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082225"
---
# <a name="manage-summary-information"></a>Administrar información de Resumen

El WiSumInf.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo se puede usar para administrar la [secuencia de información de Resumen](summary-information-stream.md) de un paquete de Windows Installer.

En el ejemplo se muestra el uso de:

-   [**Propiedad SummaryInformation (objeto Installer)**](installer-summaryinformation.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiSumInf.vbs \[ ruta de acceso a la propiedad de base de datos \] \[ = valor\]**

Especifique la ruta de acceso a la base de datos Windows Installer. Si no se especifican otros argumentos, el script muestra todas las propiedades de resumen del paquete. Especifique una lista de propiedades de Resumen y valores que se van a actualizar con el formato propiedad = valor. Puede especificar la propiedad mediante el nombre o el valor de PID que se muestra a continuación. Los campos de fecha y hora usan el formato de configuración regional actual o "ahora" o "fecha". Para obtener más información, vea [conjunto de propiedades de flujo de información de Resumen](summary-information-stream-property-set.md).



| PID | Nombre        | Descripción                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | Página de códigos ANSI de cadenas de texto en información de resumen. Para obtener más información, vea CodePage (propiedad de [**Resumen**](codepage-summary.md) ).                                                                                                                                                           |
| 2   | Título       | Tipo de Windows Installer paquete. Para obtener más información, vea [**title Summary Property**](title-summary.md).                                                                                                                                                                                    |
| 3   | Asunto     | Nombre completo del producto. Para obtener más información, vea [**Subject Summary Property**](subject-summary.md).                                                                                                                                                                                               |
| 4   | Autor      | Creador, normalmente nombre del proveedor. Para obtener más información, consulte [**Author Summary Property**](author-summary.md).                                                                                                                                                                                     |
| 5   | Palabras clave    | Lista de palabras clave para su uso por el explorador de archivos. Para obtener más información, vea [**palabra clave Summary (propiedad)**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Comentarios    | Descripción del propósito o uso del paquete. Para obtener más información, vea [**comentarios Summary Property**](comments-summary.md).                                                                                                                                                                       |
| 7   | Plantilla    | Plataformas e idiomas admitidos. Para obtener más información, consulte [**Template Summary Property**](template-summary.md).                                                                                                                                                                              |
| 8   | LastAuthor  | Lo establece solo el instalador. Para obtener más información, consulte [**Last Saved by Summary Property**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revisión    | GUID del código de paquete. Para obtener más información, consulte [**propiedad de Resumen de número de revisión**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Imprimir     | Fecha y hora de la imagen de instalación. Para obtener más información, vea [**última propiedad de Resumen impresa**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Creado     | Fecha y hora de creación del paquete. Para obtener más información, vea [**crear una propiedad de Resumen de fecha y hora**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Guardado       | Fecha y hora de la última modificación del paquete. Para obtener más información, consulte [**propiedad de Resumen de fecha y hora de la última vez**](last-saved-time-date-summary.md)que se guardó.                                                                                                                                             |
| 14  | Páginas       | Versión mínima de Windows Installer necesaria para este paquete. Para obtener más información, vea [**propiedad de Resumen de recuento de páginas**](page-count-summary.md).                                                                                                                                             |
| 15  | Palabras       | Tipo de imagen del archivo de origen. Para obtener más información, consulte [**propiedad de Resumen de recuento de palabras**](word-count-summary.md). A partir de Windows Installer versión 4,0 en Windows Vista y Windows Server 2008, esta propiedad incluye bits para especificar si se requieren privilegios elevados.<br/> |
| 16  | Characters  | Se usa solo para transformaciones. [**Recuento de caracteres**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Application | Aplicación asociada a este archivo, es decir, "Windows Installer". Para obtener más información, vea [**crear una propiedad de Resumen**](creating-application-summary.md)de la aplicación.                                                                                                                        |
| 19  | Seguridad    | Configuración de seguridad. Para obtener más información, vea [**Security Summary Property**](security-summary.md).                                                                                                                                                                                               |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




