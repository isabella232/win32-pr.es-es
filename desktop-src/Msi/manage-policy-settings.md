---
description: El archivo VBScript WiPolicy.vbs se proporciona en los componentes Windows SDK para desarrolladores Windows Installer. En este ejemplo se muestra cómo se puede usar el script para administrar la directiva del sistema. Un administrador puede configurar la directiva mediante directiva de grupo Editor de directivas (GPE).
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Administrar la configuración de directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1261c48ec7cc7e51a8556b7565075fa9e92bd60481da08f4f311a3de995a91f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945619"
---
# <a name="manage-policy-settings"></a>Administrar la configuración de directivas

El archivo vbscript WiPolicy.vbs se proporciona en los componentes del SDK de [Windows para Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo se puede usar el script para administrar la [directiva del sistema](system-policy.md). Un administrador puede configurar la directiva mediante directiva de grupo Editor de directivas (GPE).

En este ejemplo se muestran las directivas Windows Installer.

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Valor de directiva WiPolicy.vbs \[ \] \[ cscript\]**

Si no se especifica ningún argumento en la línea de comandos, el ejemplo devuelve la configuración de directiva actual. Especifique la directiva que se va a establecer mediante los siguientes códigos de identificador. Especifique el nuevo valor de la directiva. Para devolver el valor actual de una directiva, especifique una cadena vacía "" para el valor.



| CODE | Descripción                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modos de registro. Para obtener más información, vea [Registro.](logging.md)                                                                            |
| DO   | Modos de depuración. Para obtener más información, vea [Depurar](debug.md).                                                                                   |
| DI   | Deshabilite Windows installer. Para obtener más información, [vea DisableMsi](disablemsi.md).                                                      |
| Wt   | Tiempo de espera en segundos en caso de que no haya actividad. **HKLM** \\ **SoftWare** \\ **Directivas** \\ **Microsoft** \\ **Windows** \\ **Instalador** \\ **Tiempo de espera** |
| DB   | Deshabilite la exploración por parte del usuario de las ubicaciones de origen. Para obtener más información, [vea DisableBrowse](disablebrowse.md).                                     |
| DP   | Deshabilite la aplicación de revisiones. Para obtener más información, [vea DisablePatch](disablepatch.md).                                                                |
| Uc   | Propiedades públicas enviadas para instalar el servicio. Para obtener más información, [vea EnableUserControl](enableusercontrol.md).                             |
| SS   | Instalador seguro para scripting desde el explorador. Para obtener más información, [vea SafeForScripting](safeforscripting.md).                               |
| EM   | Privilegios del sistema (HKLM). Para obtener más información, [vea AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| EU   | Privilegios del sistema (HKCU). Para obtener más información, [vea AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| DR   | Deshabilite la directiva de reversión. Para obtener más información, [vea DisableRollback](disablerollback.md).                                                   |
| TS   | Busque transformaciones en la raíz de la imagen de origen. Para obtener más información, [vea TransformsAtSource policy](transformsatsource-policy.md).             |
| TP   | Anclar tranformes seguros en la caché del lado cliente. Para obtener más información, [vea TransformsSecure policy](transformssecure-policy.md).                 |
| SO   | Orden de búsqueda de tipos de origen. Para obtener más información, vea [SearchOrder](searchorder.md).                                                      |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 



