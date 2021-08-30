---
title: Recopilación de User-Mode volcados de memoria
description: A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), se puede configurar Informe de errores de Windows (WER) para que los volcados completos del modo de usuario se repunten y almacenen localmente después de que se bloquea una aplicación en modo de usuario.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890dfbe297e5448d831ce2f149777a66db5ef7e7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473061"
---
# <a name="collecting-user-mode-dumps"></a>Recopilación de User-Mode volcados de memoria

A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), se puede configurar Informe de errores de Windows (WER) para que los volcados completos del modo de usuario se repunten y almacenen localmente después de que se bloquea una aplicación en modo de usuario. Esta característica no admite las aplicaciones que hacen sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET.

Esta característica no está habilitada de manera predeterminada. La habilitación de la característica requiere privilegios de administrador. Para habilitar y configurar la característica, use los siguientes valores del Registro en la clave **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps.**


| Valor | Descripción | Tipo | Valor predeterminado | 
|-------|-------------|------|---------------|
| <strong>DumpFolder</strong> | Ruta de acceso donde se almacenarán los archivos de volcado. Si no usa la ruta de acceso predeterminada, asegúrese de que la carpeta contiene ACL que permiten al proceso de bloqueo escribir datos en la carpeta. Para los bloqueos del servicio, el volcado se escribe en carpetas de perfil específicas del servicio en función de la cuenta de servicio usada. Por ejemplo, la carpeta de perfil para los servicios del sistema es %WINDIR%\System32\Config\SystemProfile. Para Servicios locales y de red, la carpeta es %WINDIR%\ServiceProfiles.<br /> |  REG_EXPAND_SZ  | %LOCALAPPDATA%\CrashDumps | 
| <strong>DumpCount</strong> | Número máximo de archivos de volcado de memoria de la carpeta. Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado. | REG_DWORD | 10 | 
| <strong>DumpType</strong> | Especifique uno de los siguientes tipos de volcado:<ul><li>0: Volcado personalizado</li><li>1: Minivolcar</li><li>2: Volcado completo</li></ul> | REG_DWORD | 1 | 
| <strong>CustomDumpFlags</strong> | Opciones de volcado personalizadas que se usarán. Este valor solo se usa cuando <strong>DumpType</strong> está establecido en 0.<br /> Las opciones son una combinación bit a bit de los valores <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeración.<br /> | REG_DWORD | <code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code> | 


>[!NOTE]
> No se recopila un volcado de memoria cuando se [establece la depuración automática para **bloqueos de** aplicación.](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes) 

Estos valores del Registro representan la configuración global. También puede proporcionar la configuración por aplicación que invalide la configuración global. Para crear una configuración por aplicación, cree una nueva clave para la aplicación en **HKEY \_ LOCAL MACHINE Software Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps** (por ejemplo, **HKEY LOCAL MACHINE Software \_ Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**). Agregue la configuración de volcado en la **MyApplication.exe** de volcado. Si la aplicación se bloquea, WER leerá primero la configuración global y, a continuación, invalidará cualquiera de las opciones con la configuración específica de la aplicación.

Después de que una aplicación se bloquea y antes de su finalización, el sistema comprobará la configuración del Registro para determinar si se va a recopilar un volcado local. Una vez completada la recopilación de volcados, se permitirá que la aplicación finalice con normalidad. Si la aplicación admite la recuperación, el volcado local se recopila antes de llamar a la devolución de llamada de recuperación.

Estos volcados se configuran y controlan independientemente del resto de la infraestructura de WER. Puede usar la colección de volcados local incluso si WER está deshabilitado o si el usuario cancela los informes de WER. El volcado local puede ser diferente del volcado enviado a Microsoft.

 

