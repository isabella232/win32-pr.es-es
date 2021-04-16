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
# <a name="version-helper-functions"></a><span data-ttu-id="7762e-103">Funciones auxiliares de versión</span><span class="sxs-lookup"><span data-stu-id="7762e-103">Version Helper functions</span></span>

<span data-ttu-id="7762e-104">Las siguientes funciones se pueden utilizar para determinar la versión actual del sistema operativo o para identificar si se trata de una versión de Windows o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7762e-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="7762e-105">Estas funciones proporcionan pruebas sencillas que usan la función [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) y que se recomiendan las comparaciones mayor o igual que las comparadas como un medio sólido para determinar la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7762e-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="7762e-106">Estas API están definidas por **versionhelpers. h**, que se incluye en el kit de desarrollo de software (SDK) de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7762e-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="7762e-107">Este archivo se puede usar con otras versiones de Microsoft Visual Studio para implementar la misma funcionalidad para las versiones de Windows anteriores a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7762e-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7762e-108">Función</span><span class="sxs-lookup"><span data-stu-id="7762e-108">Function</span></span></th>
<th><span data-ttu-id="7762e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7762e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7762e-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-111">Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7762e-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-113">Indica si la versión actual del sistema operativo coincide con la versión de Windows XP con Service Pack 1 (SP1) o es mayor.</span><span class="sxs-lookup"><span data-stu-id="7762e-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762e-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-115">Indica si la versión actual del sistema operativo coincide con la versión de Windows XP con Service Pack 2 (SP2) o es mayor.</span><span class="sxs-lookup"><span data-stu-id="7762e-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-117">Indica si la versión del sistema operativo actual coincide con la versión de Windows XP con Service Pack 3 (SP3) o es mayor.</span><span class="sxs-lookup"><span data-stu-id="7762e-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762e-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-119">Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7762e-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-121">Indica si la versión actual del sistema operativo coincide con la versión de Windows Vista con Service Pack 1 (SP1) o es mayor que.</span><span class="sxs-lookup"><span data-stu-id="7762e-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762e-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-123">Indica si la versión del sistema operativo actual coincide con la versión de Windows Vista con Service Pack 2 (SP2) o es mayor.</span><span class="sxs-lookup"><span data-stu-id="7762e-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-125">Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7762e-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762e-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-127">Indica si la versión actual del sistema operativo coincide con la versión de Windows 7 con Service Pack 1 (SP1) o es mayor que.</span><span class="sxs-lookup"><span data-stu-id="7762e-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-129">Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7762e-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762e-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-131">Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7762e-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="7762e-132">En Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> devuelve false a menos que la aplicación contenga un manifiesto que incluya una sección de compatibilidad que contenga los GUID que designan Windows 8.1 y/o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7762e-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="7762e-134">Indica si la versión actual del sistema operativo coincide con, o es mayor que, la versión de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7762e-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="7762e-135">En Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> devuelve false a menos que la aplicación contenga un manifiesto que incluya una sección de compatibilidad que contenga el GUID que designa Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7762e-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762e-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="7762e-137">Indica si el sistema operativo actual es una versión de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7762e-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="7762e-138">Las aplicaciones que necesitan distinguir entre las versiones de cliente y servidor de Windows deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="7762e-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762e-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="7762e-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="7762e-140">Solo debe usar esta función si las otras funciones auxiliares de la versión proporcionadas no se ajustan a su escenario.</span><span class="sxs-lookup"><span data-stu-id="7762e-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="7762e-141">Indica si la versión actual del sistema operativo coincide con la información de versión proporcionada, o es mayor que.</span><span class="sxs-lookup"><span data-stu-id="7762e-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="7762e-142">Esta función es útil para confirmar una versión de Windows Server que no comparte un número de versión con una versión de cliente.</span><span class="sxs-lookup"><span data-stu-id="7762e-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="7762e-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7762e-143">Example</span></span>

<span data-ttu-id="7762e-144">Las funciones insertadas definidas en el archivo de encabezado **VersionHelpers. h** permiten comprobar la versión del sistema operativo devolviendo un valor **booleano** al probar una versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="7762e-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="7762e-145">Por ejemplo, si la aplicación requiere Windows 8 o una versión posterior, use la siguiente prueba.</span><span class="sxs-lookup"><span data-stu-id="7762e-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="7762e-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7762e-146">Related topics</span></span>

- [<span data-ttu-id="7762e-147">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="7762e-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
