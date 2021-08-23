---
description: Msistuff.exe es una utilidad de línea de comandos que se puede usar para mostrar o configurar los recursos en Setup.exe ejecutable de arranque.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a29c3fd904f137679cf1ce42f3718be151e07c3368b03e6f2807dbfc08656ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145628"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe es una utilidad de línea de comandos que se puede usar para mostrar o configurar los recursos en Setup.exe ejecutable de arranque.

Esta herramienta solo está disponible en los componentes Windows [SDK para desarrolladores Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Syntax

**msistuff setup.exe** *option{value}*

Si no se especifica ningún dato después de una opción, ese recurso se quita.

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msistuff.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guion. Si una opción aparece varias veces, solo se usa la última aparición.



| Opción               | Id. de recurso                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no se especifica ninguna opción |                              | Mostrar recursos configurables en Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME \_ BASEURL      | Establezca BaseURL, la ubicación de la dirección URL base de Setup.exe. Si no hay ningún valor, la ubicación de Setup.exe predeterminado es un medio extraíble. Solo las instalaciones basadas en direcciones URL están sujetas a una comprobación [**con WinVerifyTrust.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) La barra diagonal final de la dirección URL es opcional. Esta opción se puede omitir.                                                                                                                                                                                                                     |
| **-d**               | ISETUPPROPNAME \_ DATABASE     | Establezca Msi, el nombre del .msi archivo. Se trata de una ruta de acceso relativa al .msi en relación con la ubicación del Setup.exe programa. Esta opción es necesaria si no se especifica la opción -m. Las opciones -d y -m son mutuamente excluyentes. No se pueden especificar ambos.                                                                                                                                                                                                                                                    |
| **-m**               | REVISIÓN DE \_ ISETUPPROPNAME        | Establezca Msp, el nombre del archivo .msp. Se trata de una ruta de acceso relativa al archivo .msp en relación con la ubicación del Setup.exe programa. Esta opción es necesaria si no se especifica la opción -d. Las opciones -m y -d son mutuamente excluyentes. No se pueden especificar ambos.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ PRODUCTNAME  | Establezca Product Name (Nombre del producto), el nombre del producto. Esto proporciona el nombre usado en el texto del banner para la interfaz de usuario descargada. Esta opción se puede omitir. Si se omite, el valor predeterminado es "el producto".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | ISETUPPROPNAME \_ OPERATION    | Especifique el tipo de operación que se realizará. Los valores válidos son INSTALL, MINPATCH,PARPATCH e INSTALLUPD. Para obtener más información sobre estas opciones, vea [Internet Download Bootstrapping](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | MSI MÍNIMO DE ISETUPPROPNAME \_ \_ | Establezca Versión mínima de Msi, la versión mínima de Windows Instalador necesario en el equipo. Si la versión mínima del instalador de Windows no está [](instmsi-exe.md) presente en el equipo, se instala elInstmsi.exeadecuado para actualizar el Windows instalador. El valor de esta propiedad tiene el mismo formato que el valor \_ PAGECOUNT de PID. Consulte [**La propiedad Resumen de recuento de**](page-count-summary.md) páginas. El valor debe ser al menos 200, el valor del Windows Installer versión 2.0. Esta opción es obligatoria. |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | Establezca Ubicación de dirección URL de InstMsi, la ubicación de dirección URL base de Windows ejecutables de actualización del instalador. Si falta este valor, la ubicación de los ejecutables de actualización tiene como valor predeterminado la ubicación de Setup.exe. Esta opción se puede omitir.                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIA     | Establezca InstMsiA, el nombre de la versión ANSI de Windows ejecutable de actualización del instalador. Se trata de una ruta de acceso relativa a la versión ANSI Instmsi.exe con respecto a la ubicación especificada por ISETUPPROPNAME \_ INSTLOCATION. Esta opción es obligatoria.                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | Establezca InstMsiW, el nombre de la versión Unicode de Windows ejecutable de actualización del instalador. Se trata de una ruta de acceso relativa a la versión Unicode de Instmsi.exe con respecto a la ubicación especificada por ISETUPPROPNAME \_ INSTLOCATION. Esta opción es obligatoria.                                                                                                                                                                                                                                                                             |
| **-p**               | PROPIEDADES DE \_ ISETUPPROPNAME   | Establezca las cadenas PROPERTY=VALUE. Estos son los pares PROPERTY=VALUE que se van a incluir en la línea de comandos. Esta opción se puede omitir. Esta opción no se puede enumerar varias veces y debe aparecer en último lugar en la línea de comandos. Toda la línea de comandos siguiente a -p se considera parte de {value}.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Arranque de descarga de Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Ejemplo de instalación del instalador Windows url](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
