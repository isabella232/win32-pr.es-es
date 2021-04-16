---
description: La utilidad comprobador de archivos de sistema, Sfc.exe, permite a los administradores analizar todos los recursos protegidos para comprobar sus versiones.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Comprobador de archivos de sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669813"
---
# <a name="system-file-checker"></a><span data-ttu-id="dfab8-103">Comprobador de archivos de sistema</span><span class="sxs-lookup"><span data-stu-id="dfab8-103">System File Checker</span></span>

<span data-ttu-id="dfab8-104">La utilidad comprobador de archivos de sistema, Sfc.exe, permite a los administradores analizar todos los recursos protegidos para comprobar sus versiones.</span><span class="sxs-lookup"><span data-stu-id="dfab8-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="dfab8-105">Los archivos críticos para reiniciar Windows que no coinciden con la versión de Windows esperada pueden reemplazarse por las versiones correctas.</span><span class="sxs-lookup"><span data-stu-id="dfab8-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="dfab8-106">Si se repara un archivo, también se reparan los datos del registro correspondientes.</span><span class="sxs-lookup"><span data-stu-id="dfab8-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="dfab8-107">Los archivos protegidos no críticos para reiniciar Windows no se reparan.</span><span class="sxs-lookup"><span data-stu-id="dfab8-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfab8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfab8-108">Syntax</span></span>

<span data-ttu-id="dfab8-109">A continuación se muestra la sintaxis de línea de comandos para SFC.</span><span class="sxs-lookup"><span data-stu-id="dfab8-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="dfab8-110">**Opciones de SFC \[ = ruta de acceso completa del archivo\]**</span><span class="sxs-lookup"><span data-stu-id="dfab8-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="dfab8-111">Opciones</span><span class="sxs-lookup"><span data-stu-id="dfab8-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="dfab8-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*</span><span class="sxs-lookup"><span data-stu-id="dfab8-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-113">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-113">This value is not supported.</span></span>

<span data-ttu-id="dfab8-114">**Windows Server 2003 y Windows XP:** Establece el tamaño de la caché de archivos.</span><span class="sxs-lookup"><span data-stu-id="dfab8-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="dfab8-115">El tamaño predeterminado de la memoria caché es de 50 MB.</span><span class="sxs-lookup"><span data-stu-id="dfab8-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span><span class="sxs-lookup"><span data-stu-id="dfab8-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-117">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span><span class="sxs-lookup"><span data-stu-id="dfab8-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-119">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span><span class="sxs-lookup"><span data-stu-id="dfab8-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-121">Comprobar o reparar solo archivos.</span><span class="sxs-lookup"><span data-stu-id="dfab8-121">Verify or repair only files.</span></span> <span data-ttu-id="dfab8-122">No Compruebe ni repare las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="dfab8-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="dfab8-123">**Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span><span class="sxs-lookup"><span data-stu-id="dfab8-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-125">Use esta opción para las reparaciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dfab8-125">Use this option for offline repairs.</span></span> <span data-ttu-id="dfab8-126">Especifique la ubicación del directorio de arranque sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dfab8-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="dfab8-127">**Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span><span class="sxs-lookup"><span data-stu-id="dfab8-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-129">Use esta opción para las reparaciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dfab8-129">Use this option for offline repairs.</span></span> <span data-ttu-id="dfab8-130">Especifique la ubicación del directorio de Windows sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dfab8-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="dfab8-131">**Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span><span class="sxs-lookup"><span data-stu-id="dfab8-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-133">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-133">This value is not supported.</span></span>

<span data-ttu-id="dfab8-134">**Windows Server 2003 y Windows XP:** Vacía la memoria caché de archivos y examina todos los archivos del sistema protegidos.</span><span class="sxs-lookup"><span data-stu-id="dfab8-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span><span class="sxs-lookup"><span data-stu-id="dfab8-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-136">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span><span class="sxs-lookup"><span data-stu-id="dfab8-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-138">Vuelva a la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dfab8-138">Return to default settings.</span></span>

<span data-ttu-id="dfab8-139">**Windows Server 2008 y Windows Vista:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span><span class="sxs-lookup"><span data-stu-id="dfab8-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-141">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-141">This value is not supported.</span></span>

<span data-ttu-id="dfab8-142">**Windows Server 2003 y Windows XP:** Examina todos los archivos del sistema protegidos en cada arranque.</span><span class="sxs-lookup"><span data-stu-id="dfab8-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span><span class="sxs-lookup"><span data-stu-id="dfab8-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-144">Examina y repara el archivo que se encuentra en la ruta de acceso completa especificada.</span><span class="sxs-lookup"><span data-stu-id="dfab8-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="dfab8-145">**Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="dfab8-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-147">Examina todos los archivos del sistema protegidos inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="dfab8-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span><span class="sxs-lookup"><span data-stu-id="dfab8-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-149">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="dfab8-149">This value is not supported.</span></span>

<span data-ttu-id="dfab8-150">**Windows Server 2003 y Windows XP:** Examina todos los archivos del sistema protegidos en el siguiente arranque.</span><span class="sxs-lookup"><span data-stu-id="dfab8-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="dfab8-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-152">Comprueba el archivo en la ruta de acceso completa especificada.</span><span class="sxs-lookup"><span data-stu-id="dfab8-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="dfab8-153">Esta opción no repara el archivo.</span><span class="sxs-lookup"><span data-stu-id="dfab8-153">This option does not repair the file.</span></span>

<span data-ttu-id="dfab8-154">**Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfab8-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span><span class="sxs-lookup"><span data-stu-id="dfab8-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="dfab8-156">Examina todos los archivos del sistema protegidos, pero no repara los archivos.</span><span class="sxs-lookup"><span data-stu-id="dfab8-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="dfab8-157">**Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="dfab8-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="dfab8-158">SFC establece el siguiente valor del registro:</span><span class="sxs-lookup"><span data-stu-id="dfab8-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="dfab8-159">= HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan</span><span class="sxs-lookup"><span data-stu-id="dfab8-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="dfab8-160">Para obtener más información, consulte [valores del registro de WFP](wfp-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="dfab8-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dfab8-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfab8-161">Remarks</span></span>

<span data-ttu-id="dfab8-162">En Windows Vista únicamente, puede establecer la variable de entorno de **\_ \_ registro de seguimiento de Windows** en la ubicación de un directorio válido para recibir un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="dfab8-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="dfab8-163">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfab8-163">Examples</span></span>

<span data-ttu-id="dfab8-164">Las siguientes líneas de comandos de ejemplo son ejemplos de sintaxis sfc.exe.</span><span class="sxs-lookup"><span data-stu-id="dfab8-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="dfab8-165">**SFC/SCANNOW**</span><span class="sxs-lookup"><span data-stu-id="dfab8-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="dfab8-166">**SFC/VERIFYFILE = c: \\ Windows \\ system32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="dfab8-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="dfab8-167">**SFC/SCANFILE = d: \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**</span><span class="sxs-lookup"><span data-stu-id="dfab8-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="dfab8-168">**/VERIFYONLY de SFC/FILESONLY**</span><span class="sxs-lookup"><span data-stu-id="dfab8-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



