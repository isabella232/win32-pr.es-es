---
description: Los Windows SDK components for Windows Installer Developers (Componentes del SDK de Windows para desarrolladores de instaladores de Windows) contienen archivos VBScript que muestran cómo se usa la interfaz de automatización del instalador de Windows para modificar Windows Installer.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Windows Ejemplos de scripting del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069558"
---
# <a name="windows-installer-scripting-examples"></a>Windows Ejemplos de scripting del instalador

La [Windows SDK components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) contiene archivos VBScript que muestran cómo se usa la interfaz de automatización del instalador de Windows para modificar Windows Installer.

Los ejemplos de script identificados en este tema no son compatibles Microsoft Corporation y solo se proporcionan como una referencia potencialmente útil. La ejecución de estos ejemplos requiere Windows host de script. Para obtener más información sobre Windows host de script, vea la sección Windows [Script Host](/previous-versions//9bbdkx3k(v=vs.85)) del Kit de desarrollo de software (SDK) de Microsoft Windows.



| Archivo de script de ejemplo | Descripción                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Enumerar productos, propiedades, características y componentes](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importar archivos](import-files.md)                                                                            |
| WiExport.vbs       | [Exportar archivos](export-files.md)                                                                            |
| WiSubStg.vbs       | [Administración de subalmacenamientos](manage-substorages.md)                                                                |
| WiStream.vbs       | [Administrar archivos binarios Secuencias](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Combinar dos bases de datos](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Generar una transformación](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Aplicar una transformación](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Ver una transformación](view-a-transform.md) (solo CSCRIPT)                                                     |
| WiDiffDb.vbs       | [Ver diferencias entre dos bases de datos](view-differences-between-two-databases.md) (solo CSCRIPT)         |
| WiLstScr.vbs       | [Ver script del instalador](view-installer-script.md) (solo CSCRIPT)                                           |
| WiSumInf.vbs       | [Administrar información de resumen](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Administrar la configuración de directivas](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Administrar lenguaje y página de códigos](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Copiar un archivo Unicode en un archivo Ansi](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Administrar tamaños y versiones de archivos](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Generar archivador de archivos](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Ejecutar SQL instrucciones](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Copiar un archivo ANSI en un campo de base de datos](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Enumerar componentes](list-components.md)                                                                      |
| WiFeatur.vbs       | [Enumerar características](list-features.md)                                                                          |
| WiDialog.vbs       | [Versión preliminar Interfaz de usuario](preview-user-interface.md)                                                        |



 

Todos estos scripts muestran una pantalla de ayuda que describe sus argumentos de línea de comandos. Para mostrar la pantalla de ayuda en Windows doble clic en el archivo. Para mostrar la pantalla de ayuda desde una línea de comandos, escriba ? como primer argumento o escriba menos argumentos de los necesarios. Los scripts devuelven un valor de 0 si se ejecuta correctamente, 1 si se invoca ayuda y 2 si se produce un error.

Estos ejemplos requieren Windows host de script para ejecutarse. Windows El host de script es en realidad dos hosts:

-   CScript.exe es la versión que permite ejecutar scripts desde el símbolo del sistema y proporciona modificadores de línea de comandos para establecer las propiedades del script.
-   WScript.exe es la versión de Windows host de script que permite ejecutar scripts desde Windows. Para obtener más información, consulte [la Windows host de script](/previous-versions//9bbdkx3k(v=vs.85)) en el SDK de Windows.

La utilidad Makecab.exe se incluye con los ejemplos de aplicación de revisiones en [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Para obtener información sobre WMI, vea [Using Windows Installer with WMI](using-windows-installer-with-wmi.md).

 

 
