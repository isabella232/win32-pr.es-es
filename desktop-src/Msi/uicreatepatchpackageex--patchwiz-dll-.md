---
description: La función UiCreatePatchPackageEx toma un archivo de creación de paquetes (archivo. PCP) y genera un paquete de revisión de Windows Installer (paquete. msp). La llamada a Msimsp.exe es el método recomendado para utilizar Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677259"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="61e0d-104">UiCreatePatchPackageEx (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="61e0d-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="61e0d-105">La función UiCreatePatchPackageEx toma un archivo de creación de paquetes (archivo. PCP) y genera un paquete de revisión de Windows Installer (paquete. msp).</span><span class="sxs-lookup"><span data-stu-id="61e0d-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="61e0d-106">La llamada a [Msimsp.exe](msimsp-exe.md) es el método recomendado para utilizar [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="61e0d-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="61e0d-107">La función UiCreatePatchPackageEx está disponible a partir de Patchwiz.dll versión 4,0 y extiende la funcionalidad de la función [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="61e0d-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="61e0d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61e0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e0d-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="61e0d-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-110">Ruta de acceso completa al archivo de propiedades de creación de revisiones (archivo. PCP) para esta revisión.</span><span class="sxs-lookup"><span data-stu-id="61e0d-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="61e0d-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="61e0d-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-112">Ruta de acceso completa al paquete de revisión de Windows Installer (archivo. msp) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="61e0d-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="61e0d-113">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="61e0d-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="61e0d-114">Si es **null** o una cadena vacía, la función usa el valor de PatchOutputPath en la [tabla Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="61e0d-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="61e0d-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="61e0d-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-116">Ruta de acceso completa a un archivo de registro de texto que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="61e0d-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="61e0d-117">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="61e0d-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="61e0d-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="61e0d-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-119">Identificador de una ventana que muestra el texto de estado.</span><span class="sxs-lookup"><span data-stu-id="61e0d-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="61e0d-120">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="61e0d-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="61e0d-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="61e0d-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-122">Ubicación de los archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="61e0d-122">Location for temporary files.</span></span> <span data-ttu-id="61e0d-123">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="61e0d-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="61e0d-124">El usuario debe tener privilegios suficientes para leer y escribir en esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="61e0d-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="61e0d-125">La ubicación predeterminada es% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="61e0d-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="61e0d-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="61e0d-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-127">Si **es true**, quite la carpeta temporal y todo su contenido, si está presente.</span><span class="sxs-lookup"><span data-stu-id="61e0d-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="61e0d-128">Si es **false** y la carpeta está presente, se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="61e0d-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="61e0d-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="61e0d-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-130">Este parámetro se puede establecer en uno o en una combinación de los valores siguientes para especificar las opciones de registro o de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="61e0d-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="61e0d-131">Marca</span><span class="sxs-lookup"><span data-stu-id="61e0d-131">Flag</span></span>            | <span data-ttu-id="61e0d-132">Value</span><span class="sxs-lookup"><span data-stu-id="61e0d-132">Value</span></span>       | <span data-ttu-id="61e0d-133">Significado</span><span class="sxs-lookup"><span data-stu-id="61e0d-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="61e0d-134">LOGNONE</span><span class="sxs-lookup"><span data-stu-id="61e0d-134">LOGNONE</span></span>         | <span data-ttu-id="61e0d-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61e0d-135">0x00000000</span></span>  | <span data-ttu-id="61e0d-136">No escriba mensajes en el registro.</span><span class="sxs-lookup"><span data-stu-id="61e0d-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="61e0d-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="61e0d-137">LOGINFO</span></span>         | <span data-ttu-id="61e0d-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="61e0d-138">0x00000001</span></span>  | <span data-ttu-id="61e0d-139">Escriba mensajes informativos en el registro.</span><span class="sxs-lookup"><span data-stu-id="61e0d-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="61e0d-140">LOGWARN</span><span class="sxs-lookup"><span data-stu-id="61e0d-140">LOGWARN</span></span>         | <span data-ttu-id="61e0d-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="61e0d-141">0x00000002</span></span>  | <span data-ttu-id="61e0d-142">Escriba advertencias en el registro.</span><span class="sxs-lookup"><span data-stu-id="61e0d-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="61e0d-143">LOGERR</span><span class="sxs-lookup"><span data-stu-id="61e0d-143">LOGERR</span></span>          | <span data-ttu-id="61e0d-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="61e0d-144">0x00000004</span></span>  | <span data-ttu-id="61e0d-145">Escriba mensajes de error en el registro.</span><span class="sxs-lookup"><span data-stu-id="61e0d-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="61e0d-146">LOGPERFMESSAGES</span><span class="sxs-lookup"><span data-stu-id="61e0d-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="61e0d-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="61e0d-147">0x00000008</span></span>  | <span data-ttu-id="61e0d-148">Escriba mensajes de rendimiento en el registro.</span><span class="sxs-lookup"><span data-stu-id="61e0d-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="61e0d-149">UINONE</span><span class="sxs-lookup"><span data-stu-id="61e0d-149">UINONE</span></span>          | <span data-ttu-id="61e0d-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="61e0d-150">0x00000000f</span></span> | <span data-ttu-id="61e0d-151">No se muestra la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="61e0d-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="61e0d-152">UIALL</span><span class="sxs-lookup"><span data-stu-id="61e0d-152">UIALL</span></span>           | <span data-ttu-id="61e0d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61e0d-153">0x00000010</span></span>  | <span data-ttu-id="61e0d-154">Mostrar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="61e0d-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="61e0d-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="61e0d-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="61e0d-156">Reservado.</span><span class="sxs-lookup"><span data-stu-id="61e0d-156">Reserved.</span></span> <span data-ttu-id="61e0d-157">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="61e0d-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="61e0d-158">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="61e0d-158">Return Values</span></span>

<span data-ttu-id="61e0d-159">Vea la tabla de [valores devueltos para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="61e0d-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61e0d-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61e0d-160">Remarks</span></span>

<span data-ttu-id="61e0d-161">Para obtener un ejemplo de creación de un archivo. PCP y el uso de [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) para generar un paquete de revisión de Windows Installer, vea la sección [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="61e0d-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="61e0d-162">La creación de una revisión requiere una imagen de instalación sin comprimir, como una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="61e0d-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="61e0d-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) no genera revisiones binarias para los archivos de los archivadores.</span><span class="sxs-lookup"><span data-stu-id="61e0d-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



