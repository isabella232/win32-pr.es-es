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
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="adf62-103">Recopilación de volcados de User-Mode</span><span class="sxs-lookup"><span data-stu-id="adf62-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="adf62-104">A partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1), Informe de errores de Windows (WER) se pueden configurar para que los volcados de modo de usuario completos se recopilen y almacenen localmente después de que una aplicación de modo de usuario se bloquee.</span><span class="sxs-lookup"><span data-stu-id="adf62-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="adf62-105">Esta característica no admite las aplicaciones que realizan sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET.</span><span class="sxs-lookup"><span data-stu-id="adf62-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="adf62-106">Esta característica no está habilitada de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="adf62-106">This feature is not enabled by default.</span></span> <span data-ttu-id="adf62-107">La habilitación de la característica requiere privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="adf62-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="adf62-108">Para habilitar y configurar la característica, use los siguientes valores del registro en la clave **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ Informe de errores de Windows \\ LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="adf62-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf62-109">Value</span><span class="sxs-lookup"><span data-stu-id="adf62-109">Value</span></span></th>
<th><span data-ttu-id="adf62-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="adf62-110">Description</span></span></th>
<th><span data-ttu-id="adf62-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="adf62-111">Type</span></span></th>
<th><span data-ttu-id="adf62-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="adf62-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adf62-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="adf62-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="adf62-114">La ruta de acceso donde se almacenarán los archivos de volcado.</span><span class="sxs-lookup"><span data-stu-id="adf62-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="adf62-115">Si no utiliza la ruta de acceso predeterminada, asegúrese de que la carpeta contenga ACL que permitan que el proceso de bloqueo escriba datos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="adf62-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="adf62-116">En el caso de los bloqueos del servicio, el volcado se escribe en carpetas de perfil específicas del servicio en función de la cuenta de servicio utilizada.</span><span class="sxs-lookup"><span data-stu-id="adf62-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="adf62-117">Por ejemplo, la carpeta de Perfil de los servicios del sistema es%WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="adf62-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="adf62-118">En el caso de los servicios locales y de red, la carpeta es%WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="adf62-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="adf62-119"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="adf62-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="adf62-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="adf62-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf62-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="adf62-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="adf62-122">Número máximo de archivos de volcado en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="adf62-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="adf62-123">Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="adf62-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="adf62-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="adf62-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="adf62-125">10</span><span class="sxs-lookup"><span data-stu-id="adf62-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf62-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="adf62-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="adf62-127">Especifique uno de los siguientes tipos de volcado de memoria:</span><span class="sxs-lookup"><span data-stu-id="adf62-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="adf62-128">0: volcado de memoria personalizado</span><span class="sxs-lookup"><span data-stu-id="adf62-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="adf62-129">1: minivolcado</span><span class="sxs-lookup"><span data-stu-id="adf62-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="adf62-130">2: volcado completo</span><span class="sxs-lookup"><span data-stu-id="adf62-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="adf62-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="adf62-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="adf62-132">1</span><span class="sxs-lookup"><span data-stu-id="adf62-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf62-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="adf62-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="adf62-134">Opciones de volcado de memoria personalizadas que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="adf62-134">The custom dump options to be used.</span></span> <span data-ttu-id="adf62-135">Este valor solo se usa cuando <strong>DumpType</strong> se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="adf62-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="adf62-136">Las opciones son una combinación bit a bit de los valores de enumeración de <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="adf62-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="adf62-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="adf62-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="adf62-138">No se recopila un volcado de memoria al establecer la [depuración automática para los bloqueos de la **aplicación**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span><span class="sxs-lookup"><span data-stu-id="adf62-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="adf62-139">Estos valores del registro representan la configuración global.</span><span class="sxs-lookup"><span data-stu-id="adf62-139">These registry values represent the global settings.</span></span> <span data-ttu-id="adf62-140">También puede proporcionar una configuración por aplicación que invalide la configuración global.</span><span class="sxs-lookup"><span data-stu-id="adf62-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="adf62-141">Para crear una configuración por aplicación, cree una nueva clave para la aplicación en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ Informe de errores de Windows \\ LocalDumps** (por ejemplo, **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ Informe de errores de Windows \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="adf62-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="adf62-142">Agregue la configuración del volcado en la clave de **MyApplication.exe** .</span><span class="sxs-lookup"><span data-stu-id="adf62-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="adf62-143">Si la aplicación se bloquea, WER leerá primero la configuración global y, a continuación, invalidará cualquiera de las opciones de configuración con la configuración específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="adf62-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="adf62-144">Después de que una aplicación se bloquea y antes de su finalización, el sistema comprobará la configuración del registro para determinar si se va a recopilar un volcado de memoria local.</span><span class="sxs-lookup"><span data-stu-id="adf62-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="adf62-145">Una vez finalizada la recopilación de volcado, se permitirá que la aplicación finalice normalmente.</span><span class="sxs-lookup"><span data-stu-id="adf62-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="adf62-146">Si la aplicación admite la recuperación, se recopila el volcado local antes de que se llame a la devolución de llamada de recuperación.</span><span class="sxs-lookup"><span data-stu-id="adf62-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="adf62-147">Estos volcados de memoria se configuran y controlan independientemente del resto de la infraestructura de WER.</span><span class="sxs-lookup"><span data-stu-id="adf62-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="adf62-148">Puede usar la colección de volcado de memoria local aunque WER esté deshabilitado o si el usuario cancela el informe de WER.</span><span class="sxs-lookup"><span data-stu-id="adf62-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="adf62-149">El volcado de memoria local puede ser diferente del volcado enviado a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="adf62-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

