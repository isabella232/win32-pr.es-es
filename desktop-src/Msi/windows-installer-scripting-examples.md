---
description: Los componentes de Windows SDK para los programadores de Windows Installer contienen archivos de VBScript que muestran cómo se usa la interfaz de automatización de Windows Installer para modificar los paquetes de Windows Installer.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Ejemplos de scripting Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002193"
---
# <a name="windows-installer-scripting-examples"></a>Ejemplos de scripting Windows Installer

Los [componentes de Windows SDK para los programadores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md) contienen archivos de VBScript que muestran cómo se usa la interfaz de automatización de Windows Installer para modificar los paquetes de Windows Installer.

Los ejemplos de scripts que se identifican en este tema no son compatibles con Microsoft Corporation y se proporcionan solo como una referencia potencialmente útil. La ejecución de estos ejemplos requiere Windows Script Host. Para obtener más información acerca de Windows Script Host, consulte la sección [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) del kit de desarrollo de software (SDK) de Microsoft Windows.



| Archivo de script de ejemplo | Descripción                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Enumerar productos, propiedades, características y componentes](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importar archivos](import-files.md)                                                                            |
| WiExport.vbs       | [Exportar archivos](export-files.md)                                                                            |
| WiSubStg.vbs       | [Administrar subalmacenamientos](manage-substorages.md)                                                                |
| WiStream.vbs       | [Administrar secuencias binarias](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Fusión mediante combinación de dos bases de datos](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Generar una transformación](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Aplicar una transformación](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Ver una transformación](view-a-transform.md) (solo cscript)                                                     |
| WiDiffDb.vbs       | [Ver las diferencias entre dos bases de datos](view-differences-between-two-databases.md) (solo cscript)         |
| WiLstScr.vbs       | [Ver script del instalador](view-installer-script.md) (solo cscript)                                           |
| WiSumInf.vbs       | [Administrar información de Resumen](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Administrar la configuración de directivas](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Administrar idioma y página de códigos](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Copiar un archivo Unicode en un archivo ANSI](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Administrar versiones y tamaños de archivo](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Generar archivo. cab](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Ejecutar instrucciones SQL](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Copiar archivo ANSI en un campo de base de datos](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Enumerar componentes](list-components.md)                                                                      |
| WiFeatur.vbs       | [Enumerar características](list-features.md)                                                                          |
| WiDialog.vbs       | [Vista previa de la interfaz de usuario](preview-user-interface.md)                                                        |



 

Todos estos scripts muestran una pantalla de ayuda que describe los argumentos de la línea de comandos. Para mostrar la pantalla de ayuda en Windows, haga doble clic en el archivo. Para mostrar la pantalla de ayuda desde una línea de comandos, escriba un? como primer argumento, o escriba menos argumentos de los necesarios. Los scripts devuelven un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error.

Estos ejemplos requieren que se ejecute Windows Script Host. Windows Script Host es en realidad dos hosts:

-   CScript.exe es la versión que permite ejecutar scripts desde el símbolo del sistema y proporciona modificadores de la línea de comandos para establecer las propiedades del script.
-   WScript.exe es la versión de Windows Script Host que permite ejecutar scripts desde Windows. Para obtener más información, consulte la sección [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) en el Windows SDK.

La utilidad de Makecab.exe se incluye con los ejemplos de revisión en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).

Para obtener información acerca de WMI, consulte [uso de Windows Installer con WMI](using-windows-installer-with-wmi.md).

 

 
