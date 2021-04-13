---
description: El archivo VBScript Manifestchk.vbs es una herramienta de validación proporcionada en el kit de desarrollo de software (SDK) de Microsoft Windows que valida los archivos de manifiesto de la aplicación y el ensamblado.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423863"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

El archivo VBScript Manifestchk.vbs es una herramienta de validación proporcionada en el kit de desarrollo de software (SDK) de Microsoft Windows que valida los archivos de manifiesto de la aplicación y el ensamblado.

La ejecución de este ejemplo requiere Windows Script Host. Para obtener más información acerca de Windows Script Host, consulte la sección Windows Script Host de la Windows SDK. Windows Script Host es en realidad dos hosts. CScript.exe es la versión que permite ejecutar scripts desde el símbolo del sistema. CScript.exe proporciona modificadores de la línea de comandos para establecer las propiedades del script.

El formato de línea de comandos es el siguiente:

**Cscript el manifestchk.vbs/s:** *\[ unidad: \] \[ ruta de acceso \] schemafilename* **/m:** *\[ unidad: \] \[ ruta de acceso \] manifestfilename* **\[ /q \] /t:** *opción*

En la tabla siguiente se describen las marcas definidas para Manifestchk.vbs.



| Marca | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Especifica el nombre del archivo de esquema de manifiesto con el que validar los manifiestos. Vea el esquema en el [esquema del archivo de manifiesto](manifest-file-schema.md).                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Especifica el nombre del archivo de manifiesto que se va a validar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Suprime todos los resultados en la consola.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Especifica el tipo de archivo de manifiesto. Los valores válidos son: AM valida el [esquema del archivo de manifiesto](manifest-file-schema.md) de un manifiesto de [ensamblado](assembly-manifests.md) o un [manifiesto de aplicación](application-manifests.md)<br/> El equipo valida el [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md) de un archivo de configuración del [publicador](publisher-configuration-files.md)<br/> AC valide el esquema del archivo de configuración de la aplicación de un [archivo de configuración](application-configuration-files.md)de la aplicación.<br/> |



 

Si no se especifica la marca/q, Manifestchk.vbs muestra información detallada acerca del primer error encontrado en el archivo y muestra un mensaje que indica si el proceso de validación se realizó correctamente o no.

Esta utilidad comprueba lo siguiente:

-   Una línea de comandos válida.
-   Está instalada la versión 3 de MSXML.
-   Que el manifiesto usa XML con formato correcto.
-   Que el manifiesto acepta con el esquema proporcionado. Tenga en cuenta que Manifestchk.vbs comprueba el archivo de manifiesto basándose solo en lo que se especifica en el esquema proporcionado. Para ver un ejemplo de un esquema de manifiesto, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).

Cscript.exe devuelve un valor de 0 si el proceso de validación se realizó correctamente y 1 si no se realizó correctamente. Devuelve 2 si hay un error en un argumento de la línea de comandos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




