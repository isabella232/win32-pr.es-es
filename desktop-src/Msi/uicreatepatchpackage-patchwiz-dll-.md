---
description: La función UiCreatePatchPackage toma un archivo de creación de paquetes (archivo. PCP) y genera un paquete de revisión de Windows Installer (paquete. msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907616"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="3e70d-103">UiCreatePatchPackage (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="3e70d-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="3e70d-104">La función UiCreatePatchPackage toma un archivo de creación de paquetes (archivo. PCP) y genera un paquete de revisión de Windows Installer (paquete. msp).</span><span class="sxs-lookup"><span data-stu-id="3e70d-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="3e70d-105">La llamada a [Msimsp.exe](msimsp-exe.md) es el método recomendado para utilizar [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="3e70d-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="3e70d-106">La función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) está disponible en la versión 4,0 de Patchwiz.dll y extiende la funcionalidad de la función UiCreatePatchPackage.</span><span class="sxs-lookup"><span data-stu-id="3e70d-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="3e70d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e70d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e70d-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="3e70d-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-109">Ruta de acceso completa al archivo de propiedades de creación de revisiones (archivo. PCP) para esta revisión.</span><span class="sxs-lookup"><span data-stu-id="3e70d-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="3e70d-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-111">Ruta de acceso completa al paquete de revisión de Windows Installer (archivo. msp) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="3e70d-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="3e70d-112">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="3e70d-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="3e70d-113">Si es **null** o una cadena vacía, la función usa el valor de PatchOutputPath en la [tabla Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="3e70d-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="3e70d-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-115">Ruta de acceso completa a un archivo de registro de texto que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="3e70d-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="3e70d-116">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="3e70d-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="3e70d-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-118">Identificador de una ventana que muestra el texto de estado.</span><span class="sxs-lookup"><span data-stu-id="3e70d-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="3e70d-119">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="3e70d-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="3e70d-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-121">Ubicación de los archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="3e70d-121">Location for temporary files.</span></span> <span data-ttu-id="3e70d-122">Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="3e70d-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="3e70d-123">La ubicación predeterminada es% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="3e70d-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="3e70d-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-125">Si **es true**, quite la carpeta temporal y todo su contenido, si está presente.</span><span class="sxs-lookup"><span data-stu-id="3e70d-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="3e70d-126">Si es **false** y la carpeta está presente, se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="3e70d-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="3e70d-127">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3e70d-127">Return Values</span></span>

<span data-ttu-id="3e70d-128">Vea la tabla de [valores devueltos para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="3e70d-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e70d-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e70d-129">Remarks</span></span>

<span data-ttu-id="3e70d-130">Para obtener un ejemplo de creación de un archivo. PCP y el uso de UiCreatePatchPackage para generar un paquete de revisión de Windows Installer, vea la sección [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="3e70d-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="3e70d-131">La creación de una revisión requiere una imagen de instalación sin comprimir, como una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3e70d-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="3e70d-132">UiCreatePatchPackage no genera revisiones binarias para los archivos de los archivadores.</span><span class="sxs-lookup"><span data-stu-id="3e70d-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



