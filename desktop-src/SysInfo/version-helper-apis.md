---
description: Las siguientes funciones se pueden utilizar para determinar la versión actual del sistema operativo o para identificar si se trata de una versión de Windows o Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Funciones auxiliares de versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/23/2021
ms.locfileid: "105671851"
---
# <a name="version-helper-functions"></a>Funciones auxiliares de versión

Las siguientes funciones se pueden utilizar para determinar la versión actual del sistema operativo o para identificar si se trata de una versión de Windows o Windows Server. Estas funciones proporcionan pruebas sencillas que usan la función [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) y que se recomiendan las comparaciones mayor o igual que las comparadas como un medio sólido para determinar la versión del sistema operativo.

> [!Note]  
> Estas API están definidas por **versionhelpers. h**, que se incluye en el kit de desarrollo de software (SDK) de Windows 8.1. Este archivo se puede usar con otras versiones de Microsoft Visual Studio para implementar la misma funcionalidad para las versiones de Windows anteriores a Windows 8.1.

<table>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows XP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con la versión de Windows XP con Service Pack 1 (SP1) o es mayor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con la versión de Windows XP con Service Pack 2 (SP2) o es mayor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Indica si la versión del sistema operativo actual coincide con la versión de Windows XP con Service Pack 3 (SP3) o es mayor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows Vista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con la versión de Windows Vista con Service Pack 1 (SP1) o es mayor que.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Indica si la versión del sistema operativo actual coincide con la versión de Windows Vista con Service Pack 2 (SP2) o es mayor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con la versión de Windows 7 con Service Pack 1 (SP1) o es mayor que.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 8.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 8.1.<br/> En Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> devuelve false a menos que la aplicación contenga un manifiesto que incluya una sección de compatibilidad que contenga los GUID que designan Windows 8.1 y/o Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 10.<br/> En Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> devuelve false a menos que la aplicación contenga un manifiesto que incluya una sección de compatibilidad que contenga el GUID que designa Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>Indica si el sistema operativo actual es una versión de Windows Server. Las aplicaciones que necesitan distinguir entre las versiones de cliente y servidor de Windows deben llamar a esta función.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>Solo debe usar esta función si las otras funciones auxiliares de la versión proporcionadas no se ajustan a su escenario.</blockquote>
<br/>Indica si la versión actual del sistema operativo coincide con la información de versión proporcionada, o es mayor que. Esta función es útil para confirmar una versión de Windows Server que no comparte un número de versión con una versión de cliente.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Ejemplo

Las funciones insertadas definidas en el archivo de encabezado **VersionHelpers. h** permiten comprobar la versión del sistema operativo devolviendo un valor **booleano** al probar una versión de Windows.

Por ejemplo, si la aplicación requiere Windows 8 o una versión posterior, use la siguiente prueba.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Temas relacionados

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
