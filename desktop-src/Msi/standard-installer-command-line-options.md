---
description: Estas son las opciones de línea de comandos estándar del Instalador estándar de Microsoft (Msiexec.exe), el ejecutable que se usa para interpretar paquetes e instalar programas.
ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e
title: Opciones de configuración de Microsoft Standard Installer Command-Line
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 8e3771975cee51e08c6b4686056f8a594a566f46
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521212"
---
# <a name="microsoft-standard-installer-command-line-options"></a>Opciones de configuración de Microsoft Standard Installer Command-Line

Estas son las opciones de línea de comandos estándar para el Instalador estándar de Microsoft (Msiexec.exe), el ejecutable que se usa para interpretar paquetes e instalar productos.

Las opciones de la línea de comandos no tienen en cuenta las mayúsculas y minúsculas.

Msiexec establece un nivel de error en la devolución que corresponde a los [códigos de error del sistema](../debug/system-error-codes.md).

> [!NOTE]
> Las opciones de línea de comandos que se identifican en este tema están disponibles a partir de Windows Installer 3.0. Las Windows línea [de comandos del](command-line-options.md) instalador de aplicaciones están disponibles con Windows Installer 3.0 y versiones anteriores.

## <a name="help"></a>/help

Ayuda y opción de referencia rápida. Muestra el uso correcto del comando de instalación, incluida una lista de todos los modificadores y el comportamiento. La descripción del uso se puede mostrar en la interfaz de usuario. El uso incorrecto de cualquier opción invoca esta opción de ayuda.

La opción Windows instalador Command-Line equivalente es: `/?` .

### <a name="examples"></a>Ejemplos

`Msiexec /help`.

## <a name="quiet"></a>/quiet

Opción de visualización silenciosa. El instalador ejecuta una instalación sin mostrar una interfaz de usuario. No se muestran mensajes, mensajes ni cuadros de diálogo al usuario. El usuario no puede cancelar la instalación.

Use las `/norestart` opciones de línea de comandos estándar o para controlar los `/forcerestart` reinicios. Si no se especifica ninguna opción de reinicio, el instalador reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario.

La opción Windows instalador Command-Line equivalente es: `/qn` .

### <a name="examples"></a>Ejemplos

`Msiexec /package Application.msi /quiet`

`Msiexec /uninstall Application.msi /quiet`

`Msiexec /update msipatch.msp /quiet`

`Msiexec /uninstall msipatch.msp /package  Application.msi / quiet`

## <a name="passive"></a>/passive

Opción de visualización pasiva. El instalador muestra una barra de progreso al usuario que indica que una instalación está en curso, pero no se muestran mensajes de error ni mensajes de error al usuario. El usuario no puede cancelar la instalación.

Use las `/norestart` opciones de línea de comandos estándar o para controlar los `/forcerestart` reinicios. Si no se especifica ninguna opción de reinicio, el instalador reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario.

 La opción Windows installer Command-Line es: `/qb!` - con establecido en la línea de `REBOOTPROMPT=S` comandos.

### <a name="examples"></a>Ejemplos
`msiexec /package Application.msi /passive`

## <a name="norestart"></a>/norestart
Opción No reiniciar nunca. El instalador nunca reinicia el equipo después de la instalación.

El equivalente Windows línea de comandos del instalador se `REBOOT=ReallySuppress` ha establecido en la línea de comandos.

### <a name="examples"></a>Ejemplos
`msiexec /package Application.msi /norestart`.

## <a name="forcerestart"></a>/forcerestart

Opción reiniciar siempre. El instalador siempre reinicia el equipo después de cada instalación.

El equivalente Windows línea de comandos del instalador se `REBOOT=Force` ha establecido en la línea de comandos.

### <a name="examples"></a>Ejemplos

`msiexec /package Application.msi /forcerestart`

## <a name="promptrestart"></a>/promptrestart

Preguntar antes de reiniciar la opción. Muestra un mensaje que indica que se requiere un reinicio para completar la instalación y pregunta al usuario si debe reiniciar el sistema ahora. Esta opción no se puede combinar con la opción `/quiet`.

El equivalente Windows línea de comandos del instalador se `REBOOTPROMPT = ""` ha establecido en la línea de comandos.

## <a name="uninstall-product"></a>/uninstall (producto)

Opción Desinstale el producto. Desinstala un producto.

La opción Windows instalador Command-Line equivalente es`/x.`

### <a name="parameters"></a>Parámetros

*<Package.msi| ProductCode>*


## <a name="uninstall-patch"></a>/uninstall (revisión)

Opción de actualización de desinstalación. Desinstala una revisión de actualización.

El equivalente Windows installer Command-Line Option es: `/I` con establecido en la línea de `MSIPATCHREMOVE=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2]` comandos.

### <a name="parameters"></a>Parámetros

*/package <Package.msi | ProductCode> /uninstall [; Update2.msp | PatchGUID2]*

## <a name="log"></a>/log

Opción de registro. Escribe información de registro en un archivo de registro en la ruta de acceso existente especificada. La ruta de acceso a la ubicación del archivo de registro ya debe existir. El instalador no crea la estructura de directorios para el archivo de registro.

Para obtener más información sobre todos los métodos disponibles para establecer el modo de registro, vea [Registro normal](normal-logging.md)Windows instalador.  

La opción Windows instalador Command-Line equivalente es: `/L*` .

La siguiente información se introduce en el registro:

- Mensajes de estado
- Advertencias nofatales
- Todos los mensajes de error
- Inicio de acciones
- Registros específicos de la acción
- Solicitudes de usuario
- Parámetros iniciales de la interfaz de usuario
- Información de salida irresal o de memoria
- Mensajes de espacio fuera del disco
- Propiedades del terminal

## <a name="package"></a>/package

Instalación de la opción de producto. Instala o configura un producto.

La opción Windows instalador Command-Line equivalente es: `/I` .

### <a name="parameters"></a>Parámetros

*<Package.msi| ProductCode>*

## <a name="update"></a>/update

Opción Instalar revisiones. Instala una o varias revisiones.

La línea de comandos Windows Installer equivalente tiene PATCH = [msipatch.msp]<; PatchGuid2> en la línea de comandos.

### <a name="parameters"></a>Parámetros

*[; Update2.msp]*
