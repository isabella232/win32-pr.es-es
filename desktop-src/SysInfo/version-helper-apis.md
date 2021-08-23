---
description: Las funciones siguientes se pueden usar para determinar la versión actual del sistema operativo o para identificar si se trata de una versión Windows o Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Funciones del asistente de versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7156070e9c793e537d976c82a632142e04cd6669b110b7d0b9fc8da95671b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884176"
---
# <a name="version-helper-functions"></a>Funciones del asistente de versiones

Las funciones siguientes se pueden usar para determinar la versión actual del sistema operativo o para identificar si se trata de una versión Windows o Windows Server. Estas funciones proporcionan pruebas sencillas que usan la función [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) y las comparaciones recomendadas mayores o iguales que se han demostrado como medios sólidos para determinar la versión del sistema operativo.

> [!Note]  
> Estas API se definen mediante **versionhelpers.h**, que se incluye en el kit de desarrollo Windows 8.1 software (SDK). Este archivo se puede usar con otras versiones Microsoft Visual Studio para implementar la misma funcionalidad para Windows versiones anteriores a Windows 8.1.

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
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la Windows XP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows XP con Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows XP con Service Pack 3 (SP3).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la Windows Vista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows Vista con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows Vista con Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la versión Windows 7 con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la Windows 8 actual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la Windows 8.1 actual.<br/> Por Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> devuelve false a menos que la aplicación contenga un manifiesto que incluya una sección de compatibilidad que contenga los GUID que designan Windows 8.1 o Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Indica si la versión actual del sistema operativo coincide o es mayor que la Windows 10 actual.<br/> Por Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> devuelve false a menos que la aplicación contenga un manifiesto que incluya una sección de compatibilidad que contenga el GUID que designa Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>Indica si el sistema operativo actual es una versión Windows Server. Las aplicaciones que necesitan distinguir entre las versiones de servidor y cliente Windows deben llamar a esta función.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>Solo debe usar esta función si las otras funciones auxiliares de versión proporcionadas no se ajustan a su escenario.</blockquote>
<br/>Indica si la versión actual del sistema operativo coincide o es mayor que la información de versión proporcionada. Esta función es útil para confirmar una versión de Windows Server que no comparte un número de versión con una versión de cliente.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Ejemplo

Las funciones insertadas definidas en el archivo de encabezado **VersionHelpers.h** permiten comprobar la versión del sistema operativo devolviendo un valor booleano al probar una versión de Windows. 

Por ejemplo, si la aplicación requiere Windows 8 o posterior, use la siguiente prueba.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Temas relacionados

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
