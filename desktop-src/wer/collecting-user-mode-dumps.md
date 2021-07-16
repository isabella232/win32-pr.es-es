---
title: Recopilación de User-Mode volcados de memoria
description: A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), se puede configurar Informe de errores de Windows (WER) para que los volcados completos del modo de usuario se repunten y almacenen localmente después de que se bloquea una aplicación en modo de usuario.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6291d3ad8dfeb641582a93f6789ca7844594ad
ms.sourcegitcommit: 892997f4126d44df413286074e08a9c6065313ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2021
ms.locfileid: "114300190"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="486df-103">Recopilación de User-Mode volcados de memoria</span><span class="sxs-lookup"><span data-stu-id="486df-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="486df-104">A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), se puede configurar Informe de errores de Windows (WER) para que los volcados completos del modo de usuario se repunten y almacenen localmente después de que se bloquea una aplicación en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="486df-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="486df-105">Las aplicaciones que hacen sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET, no son compatibles con esta característica.</span><span class="sxs-lookup"><span data-stu-id="486df-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="486df-106">Esta característica no está habilitada de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="486df-106">This feature is not enabled by default.</span></span> <span data-ttu-id="486df-107">La habilitación de la característica requiere privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="486df-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="486df-108">Para habilitar y configurar la característica, use los siguientes valores del Registro en la clave **HKEY \_ LOCAL MACHINE SOFTWARE de Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ localDumps.**</span><span class="sxs-lookup"><span data-stu-id="486df-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="486df-109">Value</span><span class="sxs-lookup"><span data-stu-id="486df-109">Value</span></span></th>
<th><span data-ttu-id="486df-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="486df-110">Description</span></span></th>
<th><span data-ttu-id="486df-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="486df-111">Type</span></span></th>
<th><span data-ttu-id="486df-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="486df-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="486df-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="486df-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="486df-114">Ruta de acceso donde se almacenarán los archivos de volcado.</span><span class="sxs-lookup"><span data-stu-id="486df-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="486df-115">Si no usa la ruta de acceso predeterminada, asegúrese de que la carpeta contiene ACL que permiten al proceso de bloqueo escribir datos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="486df-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="486df-116">Para los bloqueos de servicio, el volcado se escribe en carpetas de perfil específicas del servicio en función de la cuenta de servicio usada.</span><span class="sxs-lookup"><span data-stu-id="486df-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="486df-117">Por ejemplo, la carpeta de perfil para los servicios del sistema es %WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="486df-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="486df-118">Para servicios locales y de red, la carpeta es %WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="486df-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="486df-119"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="486df-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="486df-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="486df-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="486df-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="486df-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="486df-122">Número máximo de archivos de volcado de memoria de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="486df-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="486df-123">Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado.</span><span class="sxs-lookup"><span data-stu-id="486df-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="486df-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="486df-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="486df-125">10</span><span class="sxs-lookup"><span data-stu-id="486df-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="486df-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="486df-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="486df-127">Especifique uno de los siguientes tipos de volcado de memoria:</span><span class="sxs-lookup"><span data-stu-id="486df-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="486df-128">0: Volcado personalizado</span><span class="sxs-lookup"><span data-stu-id="486df-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="486df-129">1: Minivolcar</span><span class="sxs-lookup"><span data-stu-id="486df-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="486df-130">2: Volcado completo</span><span class="sxs-lookup"><span data-stu-id="486df-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="486df-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="486df-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="486df-132">1</span><span class="sxs-lookup"><span data-stu-id="486df-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="486df-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="486df-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="486df-134">Opciones de volcado personalizadas que se usarán.</span><span class="sxs-lookup"><span data-stu-id="486df-134">The custom dump options to be used.</span></span> <span data-ttu-id="486df-135">Este valor solo se usa cuando <strong>DumpType</strong> se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="486df-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="486df-136">Las opciones son una combinación bit a bit de los valores <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeración.</span><span class="sxs-lookup"><span data-stu-id="486df-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="486df-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="486df-137">REG_DWORD</span></span></td>
 <td><span data-ttu-id="486df-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span><span class="sxs-lookup"><span data-stu-id="486df-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span></span></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="486df-139">No se recopila un volcado de memoria cuando se [establece la depuración automática para **bloqueos** de aplicación.](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)</span><span class="sxs-lookup"><span data-stu-id="486df-139">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="486df-140">Estos valores del Registro representan la configuración global.</span><span class="sxs-lookup"><span data-stu-id="486df-140">These registry values represent the global settings.</span></span> <span data-ttu-id="486df-141">También puede proporcionar la configuración por aplicación que invalide la configuración global.</span><span class="sxs-lookup"><span data-stu-id="486df-141">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="486df-142">Para crear una configuración por aplicación, cree una nueva clave para la aplicación en **HKEY \_ LOCAL MACHINE Software Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps** (por ejemplo, **HKEY LOCAL MACHINE Software \_ Microsoft Windows Informe de errores de Windows \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="486df-142">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="486df-143">Agregue la configuración de volcado de memoria en **laMyApplication.exe** clave.</span><span class="sxs-lookup"><span data-stu-id="486df-143">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="486df-144">Si la aplicación se bloquea, WER leerá primero la configuración global y, a continuación, invalidará cualquiera de las opciones con la configuración específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="486df-144">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="486df-145">Después de que una aplicación se bloquea y antes de su finalización, el sistema comprobará la configuración del Registro para determinar si se va a recopilar un volcado local.</span><span class="sxs-lookup"><span data-stu-id="486df-145">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="486df-146">Una vez completada la recopilación de volcados, se permitirá que la aplicación finalice con normalidad.</span><span class="sxs-lookup"><span data-stu-id="486df-146">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="486df-147">Si la aplicación admite la recuperación, el volcado local se recopila antes de llamar a la devolución de llamada de recuperación.</span><span class="sxs-lookup"><span data-stu-id="486df-147">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="486df-148">Estos volcados de memoria se configuran y controlan independientemente del resto de la infraestructura de WER.</span><span class="sxs-lookup"><span data-stu-id="486df-148">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="486df-149">Puede usar la colección de volcados local incluso si WER está deshabilitado o si el usuario cancela los informes de WER.</span><span class="sxs-lookup"><span data-stu-id="486df-149">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="486df-150">El volcado local puede ser diferente del volcado enviado a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="486df-150">The local dump can be different than the dump sent to Microsoft.</span></span>

 

