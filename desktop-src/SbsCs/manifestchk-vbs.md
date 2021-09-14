---
description: El archivo VBScript Manifestchk.vbs es una herramienta de validación proporcionada en el Kit de desarrollo de software (SDK) de Microsoft Windows que valida los archivos de manifiesto de aplicación y ensamblado.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168997"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

El archivo VBScript Manifestchk.vbs es una herramienta de validación proporcionada en el Kit de desarrollo de software (SDK) de Microsoft Windows que valida los archivos de manifiesto de aplicación y ensamblado.

La ejecución de este ejemplo requiere Windows host de script. Para obtener más información sobre Windows host de script, consulte la Windows host de script del SDK de Windows. Windows El host de script es en realidad dos hosts. CScript.exe es la versión que permite ejecutar scripts desde el símbolo del sistema. CScript.exe proporciona modificadores de línea de comandos para establecer las propiedades del script.

El formato de línea de comandos es el siguiente:

**Cscript //nologo manifestchk.vbs /s:** *\[ unidad: \] \[ path \] schemafilename* **/m:** *\[ unidad: \] \[ path \] manifestfilename* **\[ /q \] /t:** *option*

Las marcas definidas para Manifestchk.vbs se describen en la tabla siguiente.



| Marca | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Especifica el nombre del archivo de esquema de manifiesto con el que se validarán los manifiestos. Vea el esquema en Esquema [de archivo de manifiesto.](manifest-file-schema.md)                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Especifica el nombre del archivo de manifiesto que se validará.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Suprime todas las salidas de la consola.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Especifica el tipo de archivo de manifiesto. Los valores válidos son: AM Validate the [manifest file schema](manifest-file-schema.md) of an assembly manifest [or](assembly-manifests.md) [application manifest](application-manifests.md)<br/> PC Valide el [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md) de un archivo de configuración del [publicador](publisher-configuration-files.md)<br/> AC Valide el esquema del archivo de configuración de la aplicación de [un archivo de configuración de la aplicación](application-configuration-files.md).<br/> |



 

Si no se especifica la marca /q, Manifestchk.vbs muestra información detallada sobre el primer error encontrado en el archivo y muestra un mensaje que indica si el proceso de validación se ha realizado correctamente o no.

Esta utilidad comprueba lo siguiente:

-   Línea de comandos válida.
-   Esa MSXML versión 3 está instalada.
-   Que el manifiesto usa XML bien formado.
-   Que el manifiesto está de acuerdo con el esquema proporcionado. Tenga en cuenta Manifestchk.vbs comprueba el archivo de manifiesto basándose solo en lo que se especifica en el esquema proporcionado. Para obtener un ejemplo de un esquema de manifiesto, vea [Esquema de archivo de manifiesto.](manifest-file-schema.md)

Cscript.exe devuelve un valor de 0 si el proceso de validación se ha realizado correctamente y 1 si no se ha realizado correctamente. Devuelve 2 si hay un error en un argumento de línea de comandos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




