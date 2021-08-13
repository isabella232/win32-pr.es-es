---
title: Recopilación de User-Mode volcados de memoria
description: A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), se puede configurar Informe de errores de Windows (WER) para que los volcados completos del modo de usuario se repunten y almacenen localmente después de que se bloquea una aplicación en modo de usuario.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4597c4bf1fd583b647e7ad74b7f1cb2cd41be9c0118226d502932c61f481cedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442369"
---
# <a name="collecting-user-mode-dumps"></a>Recopilación de User-Mode volcados de memoria

A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), se puede configurar Informe de errores de Windows (WER) para que los volcados completos del modo de usuario se repunten y almacenen localmente después de que se bloquea una aplicación en modo de usuario. Esta característica no admite las aplicaciones que hacen sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET.

Esta característica no está habilitada de manera predeterminada. La habilitación de la característica requiere privilegios de administrador. Para habilitar y configurar la característica, use los siguientes valores del Registro en la clave **HKEY \_ LOCAL MACHINE SOFTWARE microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps.**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
<th>Tipo</th>
<th>Valor predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>DumpFolder</strong></td>
<td>Ruta de acceso donde se almacenarán los archivos de volcado. Si no usa la ruta de acceso predeterminada, asegúrese de que la carpeta contiene ACL que permiten al proceso de bloqueo escribir datos en la carpeta. Para los bloqueos del servicio, el volcado se escribe en carpetas de perfil específicas del servicio en función de la cuenta de servicio usada. Por ejemplo, la carpeta de perfil para los servicios del sistema es %WINDIR%\System32\Config\SystemProfile. Para Servicios locales y de red, la carpeta es %WINDIR%\ServiceProfiles.<br/></td>
<td> REG_EXPAND_SZ </td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>Número máximo de archivos de volcado de memoria de la carpeta. Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>Especifique uno de los siguientes tipos de volcado:
<ul>
<li>0: Volcado personalizado</li>
<li>1: Minivolcar</li>
<li>2: Volcado completo</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>Opciones de volcado personalizadas que se usarán. Este valor solo se usa cuando <strong>DumpType</strong> está establecido en 0.<br/> Las opciones son una combinación bit a bit de los valores <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeración.<br/></td>
<td>REG_DWORD</td>
 <td><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> No se recopila un volcado de memoria cuando se [establece la depuración automática para **bloqueos de** aplicación.](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes) 

Estos valores del Registro representan la configuración global. También puede proporcionar la configuración por aplicación que invalide la configuración global. Para crear una configuración por aplicación, cree una nueva clave para la aplicación en **HKEY \_ LOCAL MACHINE Software Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps** (por ejemplo, **HKEY LOCAL MACHINE Software \_ Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**). Agregue la configuración de volcado bajo la **MyApplication.exe** de volcado. Si la aplicación se bloquea, WER leerá primero la configuración global y, a continuación, invalidará cualquiera de las opciones con la configuración específica de la aplicación.

Después de que una aplicación se bloquea y antes de su finalización, el sistema comprobará la configuración del Registro para determinar si se va a recopilar un volcado local. Una vez completada la recopilación de volcados, la aplicación podrá finalizar con normalidad. Si la aplicación admite la recuperación, el volcado local se recopila antes de llamar a la devolución de llamada de recuperación.

Estos volcados se configuran y controlan independientemente del resto de la infraestructura de WER. Puede usar la colección de volcados local incluso si WER está deshabilitado o si el usuario cancela los informes de WER. El volcado local puede ser diferente del volcado enviado a Microsoft.

 

