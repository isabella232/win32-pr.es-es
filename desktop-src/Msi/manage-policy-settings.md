---
description: El WiPolicy.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo muestra cómo se puede usar el script para administrar la Directiva del sistema. Un administrador puede configurar la Directiva mediante el editor de directiva de grupo (GPE).
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Administrar la configuración de directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86684e75e09fa0a588c2d1d0d999488d6e89fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677465"
---
# <a name="manage-policy-settings"></a>Administrar la configuración de directivas

El WiPolicy.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se puede usar el script para administrar la [Directiva del sistema](system-policy.md). Un administrador puede configurar la Directiva mediante el editor de directiva de grupo (GPE).

Este ejemplo muestra las directivas de Windows Installer.

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**valor de la Directiva cscript WiPolicy.vbs \[ \] \[\]**

Si no se especifica ningún argumento en la línea de comandos, el ejemplo devuelve la configuración actual de la Directiva. Especifique la Directiva que se va a establecer con los siguientes códigos de identificador. Especifique el nuevo valor para la Directiva. Para devolver el valor actual de una directiva, especifique una cadena vacía "" para el valor.



| CODE | Descripción                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modos de registro. Para obtener más información, consulte [registro](logging.md) .                                                                            |
| DO   | Modos de depuración. Para obtener más información, vea [depurar](debug.md).                                                                                   |
| DI   | Deshabilitar el modo de Windows Installer. Para obtener más información, vea [DisableMsi](disablemsi.md).                                                      |
| WT   | Tiempo de espera en segundos en el caso de ninguna actividad. **HKLM** \\ **Software** \\ de **Directivas** \\ de **Microsoft** \\ **Windows** \\ **Instalador** \\ de **Tiempo de espera** |
| DB   | Deshabilitar la exploración del usuario de las ubicaciones de origen. Para obtener más información, vea [DisableBrowse](disablebrowse.md).                                     |
| DP   | Deshabilite la revisión. Para obtener más información, vea [DisablePatch](disablepatch.md).                                                                |
| UC   | Propiedades públicas enviadas al servicio de instalación. Para obtener más información, vea [EnableUserControl](enableusercontrol.md).                             |
| SS   | Instalador seguro para scripting desde el explorador. Para obtener más información, vea [SafeForScripting](safeforscripting.md).                               |
| EM   | Privilegios del sistema (HKLM). Para obtener más información, consulte [AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| EU   | Privilegios del sistema (HKCU). Para obtener más información, consulte [AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| DR   | Deshabilite la Directiva de reversión. Para obtener más información, vea [DisableRollback](disablerollback.md).                                                   |
| TS   | Busque transformaciones en la raíz de la imagen de origen. Para obtener más información, consulte [TransformsAtSource Policy](transformsatsource-policy.md).             |
| TP   | Ancle Secure transforma en la caché del lado cliente. Para obtener más información, consulte [TransformsSecure Policy](transformssecure-policy.md).                 |
| SO   | Orden de búsqueda de tipos de origen. Para obtener más información, vea [SearchOrder](searchorder.md).                                                      |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 



