---
title: Recopilación de volcados de User-Mode
description: A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), Informe de errores de Windows (WER) se pueden configurar para que los volcados de modo de usuario completos se recopilen y almacenen localmente después de que una aplicación de modo de usuario se bloquee.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904513"
---
# <a name="collecting-user-mode-dumps"></a>Recopilación de volcados de User-Mode

A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), Informe de errores de Windows (WER) se pueden configurar para que los volcados de modo de usuario completos se recopilen y almacenen localmente después de que una aplicación de modo de usuario se bloquee. Esta característica no admite las aplicaciones que realizan sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET.

Esta característica no está habilitada de manera predeterminada. La habilitación de la característica requiere privilegios de administrador. Para habilitar y configurar la característica, use los siguientes valores del registro en la clave **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ Informe de errores de Windows \\ LocalDumps** .

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
<td>La ruta de acceso donde se almacenarán los archivos de volcado. Si no utiliza la ruta de acceso predeterminada, asegúrese de que la carpeta contenga ACL que permitan que el proceso de bloqueo escriba datos en la carpeta. En el caso de los bloqueos del servicio, el volcado se escribe en carpetas de perfil específicas del servicio en función de la cuenta de servicio utilizada. Por ejemplo, la carpeta de Perfil de los servicios del sistema es%WINDIR%\System32\Config\SystemProfile. En el caso de los servicios locales y de red, la carpeta es%WINDIR%\ServiceProfiles.<br/></td>
<td> REG_EXPAND_SZ </td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>Número máximo de archivos de volcado en la carpeta. Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado de memoria.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>Especifique uno de los siguientes tipos de volcado de memoria:
<ul>
<li>0: volcado de memoria personalizado</li>
<li>1: minivolcado</li>
<li>2: volcado completo</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>Opciones de volcado de memoria personalizadas que se van a utilizar. Este valor solo se usa cuando <strong>DumpType</strong> se establece en 0.<br/> Las opciones son una combinación bit a bit de los valores de enumeración de <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .<br/></td>
<td>REG_DWORD</td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> No se recopila un volcado de memoria al establecer la [depuración automática para los bloqueos de la **aplicación**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes). 

Estos valores del registro representan la configuración global. También puede proporcionar una configuración por aplicación que invalide la configuración global. Para crear una configuración por aplicación, cree una nueva clave para la aplicación en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ Informe de errores de Windows \\ LocalDumps** (por ejemplo, **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ Informe de errores de Windows \\ LocalDumps \\MyApplication.exe**). Agregue la configuración del volcado en la clave de **MyApplication.exe** . Si la aplicación se bloquea, WER leerá primero la configuración global y, a continuación, invalidará cualquiera de las opciones de configuración con la configuración específica de la aplicación.

Después de que una aplicación se bloquea y antes de su finalización, el sistema comprobará la configuración del registro para determinar si se va a recopilar un volcado de memoria local. Una vez finalizada la recopilación de volcado, se permitirá que la aplicación finalice normalmente. Si la aplicación admite la recuperación, se recopila el volcado local antes de que se llame a la devolución de llamada de recuperación.

Estos volcados de memoria se configuran y controlan independientemente del resto de la infraestructura de WER. Puede usar la colección de volcado de memoria local aunque WER esté deshabilitado o si el usuario cancela el informe de WER. El volcado de memoria local puede ser diferente del volcado enviado a Microsoft.

 

