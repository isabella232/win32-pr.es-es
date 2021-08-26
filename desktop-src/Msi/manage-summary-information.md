---
description: El archivo VBScript WiSumInf.vbs se proporciona en los componentes Windows SDK para desarrolladores Windows Installer. Este script de ejemplo se puede usar para administrar el flujo de información de resumen de un Windows Installer.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Administrar información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5ad72ee4f308831077ec2f732b92a70f407c560b204d10f2d3db63d1bb9bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926975"
---
# <a name="manage-summary-information"></a>Administrar información de resumen

El archivo vbscript WiSumInf.vbs se proporciona en los componentes del SDK de [Windows para Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) Este script de ejemplo se puede usar para administrar el flujo [de información de resumen](summary-information-stream.md) de un Windows Installer.

En el ejemplo se muestra el uso de:

-   [**Propiedad SummaryInformation (objeto Installer)**](installer-summaryinformation.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**cscript WiSumInf.vbs \[ ruta de acceso a la base de datos \] \[ Property=value\]**

Especifique la ruta de acceso a la base Windows del instalador. Si no se especifica ningún otro argumento, el script enumera todas las propiedades de resumen del paquete. Especifique una lista de propiedades y valores de resumen que se actualizarán con el formato Property=value. Puede especificar la propiedad por el nombre o el valor pid que se muestra a continuación. Los campos de fecha y hora usan el formato de configuración regional actual o "Now" o "Date". Para obtener más información, vea [Summary Information Stream Property Set](summary-information-stream-property-set.md).



| PID | Nombre        | Descripción                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | Página de códigos ANSI de cadenas de texto en información de resumen. Para obtener más información, vea [**Codepage Summary**](codepage-summary.md) Property.                                                                                                                                                           |
| 2   | Título       | Tipo de Windows paquete del instalador. Para obtener más información, vea [**Title Summary Property**](title-summary.md).                                                                                                                                                                                    |
| 3   | Asunto     | Nombre completo del producto . Para obtener más información, vea [**Subject Summary Property**](subject-summary.md).                                                                                                                                                                                               |
| 4   | Autor      | Creador, normalmente nombre del proveedor. Para obtener más información, vea [**Author Summary Property**](author-summary.md).                                                                                                                                                                                     |
| 5   | Palabras clave    | Lista de palabras clave para usarlas en el explorador de archivos. Para obtener más información, vea [**Keywords Summary Property**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Comentarios    | Descripción del propósito o uso del paquete. Para obtener más información, vea [**Comments Summary Property**](comments-summary.md).                                                                                                                                                                       |
| 7   | Plantilla    | Plataformas y lenguajes admitidos. Para obtener más información, vea [**Template Summary Property**](template-summary.md).                                                                                                                                                                              |
| 8   | LastAuthor  | Solo lo establece el instalador. Para obtener más información, vea [**Last Saved By Summary Property**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revisión    | GUID del código del paquete. Para obtener más información, vea [**Revision Number Summary Property**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Impreso     | Fecha y hora de la imagen de instalación. Para obtener más información, vea [**Last Printed Summary Property**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Creado     | Fecha y hora de creación del paquete. Para obtener más información, vea [**Create Time/Date Summary Property**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Guardado       | Fecha y hora de la última modificación del paquete. Para obtener más información, vea [**Last Saved Time/Date Summary Property**](last-saved-time-date-summary.md).                                                                                                                                             |
| 14  | Páginas       | Versión mínima de Windows Instalador necesario para este paquete. Para obtener más información, vea [**Page Count Summary Property**](page-count-summary.md).                                                                                                                                             |
| 15  | Palabras       | Tipo de imagen de archivo de origen. Para obtener más información, vea [**Word Count Summary Property**](word-count-summary.md). A partir de Windows Installer versión 4.0 en Windows Vista y Windows Server 2008, esta propiedad incluye bits para especificar si se requieren privilegios elevados.<br/> |
| 16  | Characters  | Solo se usa para transformaciones. [**Recuento de caracteres.**](character-count-summary.md)                                                                                                                                                                                                                    |
| 18  | Application | Aplicación asociada a este archivo, es decir, "Windows Installer". Para obtener más información, vea [**Creating Application Summary Property**](creating-application-summary.md).                                                                                                                        |
| 19  | Seguridad    | Configuración de seguridad. Para obtener más información, vea [**Security Summary Property**](security-summary.md).                                                                                                                                                                                               |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




