---
description: Msistuff.exe es una utilidad de línea de comandos que se puede usar para mostrar o configurar los recursos del ejecutable Setup.exe bootstrap.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56d6b183128971501fd3ad8ddb7a88d08cee70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668267"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe es una utilidad de línea de comandos que se puede usar para mostrar o configurar los recursos del ejecutable Setup.exe bootstrap.

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintaxis

**msistuff setup.exe** *opción {valor}*

Si no se especifica ningún dato después de una opción, se quita ese recurso.

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msistuff.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión. Si una opción se muestra varias veces, solo se usa la última aparición.



| Opción               | Id. de recurso                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no se especificaron opciones |                              | Mostrar recursos configurables en Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME \_ BASEURL      | Establezca BaseURL, la ubicación de la dirección URL base de Setup.exe. Si no hay ningún valor, la ubicación de Setup.exe toma como valor predeterminado el medio extraíble. Solo las instalaciones basadas en direcciones URL están sujetas a una comprobación con [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust). La barra diagonal final de la dirección URL es opcional. Esta opción puede omitirse.                                                                                                                                                                                                                     |
| **-d**               | \_base de datos ISETUPPROPNAME     | Establezca MSI, el nombre del archivo. msi. Se trata de una ruta de acceso relativa al archivo. msi en relación con la ubicación del programa Setup.exe. Esta opción es necesaria si no se especifica la opción-m. Las opciones-d y-m son mutuamente excluyentes. No se pueden especificar ambos.                                                                                                                                                                                                                                                    |
| **-m**               | revisión de ISETUPPROPNAME \_        | Establezca MSP, el nombre del archivo. msp. Se trata de una ruta de acceso relativa al archivo. MSP en relación con la ubicación del programa Setup.exe. Esta opción es necesaria si no se especifica la opción-d. Las opciones-m y-d son mutuamente excluyentes. No se pueden especificar ambos.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ NombreProducto  | Establezca el nombre del producto, el nombre del producto. Esto proporciona el nombre usado en el texto del titular para la interfaz de usuario descargada. Esta opción puede omitirse. Si se omite, el valor predeterminado es "el producto".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | \_operación ISETUPPROPNAME    | Especifique el tipo de operación que se va a realizar. Los valores válidos son INSTALL, MINPATCH, MAJPATCH y INSTALLUPD. Para obtener más información sobre estas opciones, consulte [arranque de descarga en Internet](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | \_MSI ISETUPPROPNAME mínimo \_ | Establezca la versión mínima de MSI, la versión mínima de Windows Installer necesaria en el equipo. Si la versión mínima del Windows Installer no está presente en el equipo, se instala el [Instmsi.exe](instmsi-exe.md) adecuado para actualizar el Windows Installer. El valor de esta propiedad tiene el mismo formato que el valor de ID. de la de PID \_ . Consulte propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) . El valor debe ser al menos 200, el valor de la Windows Installer versión 2,0. Esta opción es obligatoria. |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | Establezca la ubicación de la dirección URL de InstMsi, la ubicación de la dirección URL base de Windows Installer ejecutables de actualización. Si falta este valor, la ubicación de los archivos ejecutables de actualización tiene como valor predeterminado la ubicación de Setup.exe. Esta opción puede omitirse.                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIA     | Set InstMsiA, el nombre de la versión ANSI de Windows Installer ejecutable de actualización. Se trata de una ruta de acceso relativa a la versión ANSI de Instmsi.exe relativa a la ubicación especificada por ISETUPPROPNAME \_ INSTLOCATION. Esta opción es obligatoria.                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | Establezca InstMsiW, el nombre de la versión Unicode de Windows Installer ejecutable de actualización. Se trata de una ruta de acceso relativa a la versión Unicode de Instmsi.exe relativa a la ubicación especificada por ISETUPPROPNAME \_ INSTLOCATION. Esta opción es obligatoria.                                                                                                                                                                                                                                                                             |
| **-p**               | propiedades de ISETUPPROPNAME \_   | Establezca las cadenas PROPERTY = VALUE. Estos son los pares propiedad = valor que se van a incluir en la línea de comandos. Esta opción puede omitirse. Esta opción no se puede enumerar varias veces y debe aparecer en último lugar en la línea de comandos. Toda la línea de comandos siguiente a-p se considera como parte de {Value}.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Arranque de descarga de Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Una dirección URL basada Windows Installer ejemplo de instalación](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
