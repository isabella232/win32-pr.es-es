---
description: La \_ tabla UpgradedFile OptionalData contiene información sobre los archivos específicos de una imagen actualizada. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Tabla UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279008"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="72ccc-104">UpgradedFiles \_ OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="72ccc-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="72ccc-105">La \_ tabla UpgradedFile OptionalData contiene información sobre los archivos específicos de una imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="72ccc-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="72ccc-106">Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="72ccc-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="72ccc-107">La \_ tabla UpgradedFile OptionalData tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="72ccc-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="72ccc-108">Columna</span><span class="sxs-lookup"><span data-stu-id="72ccc-108">Column</span></span>                  | <span data-ttu-id="72ccc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="72ccc-109">Type</span></span>    | <span data-ttu-id="72ccc-110">Clave</span><span class="sxs-lookup"><span data-stu-id="72ccc-110">Key</span></span> | <span data-ttu-id="72ccc-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="72ccc-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="72ccc-112">Upgraded</span><span class="sxs-lookup"><span data-stu-id="72ccc-112">Upgraded</span></span>                | <span data-ttu-id="72ccc-113">text</span><span class="sxs-lookup"><span data-stu-id="72ccc-113">text</span></span>    | <span data-ttu-id="72ccc-114">Y</span><span class="sxs-lookup"><span data-stu-id="72ccc-114">Y</span></span>   | <span data-ttu-id="72ccc-115">N</span><span class="sxs-lookup"><span data-stu-id="72ccc-115">N</span></span>        |
| <span data-ttu-id="72ccc-116">FTK</span><span class="sxs-lookup"><span data-stu-id="72ccc-116">FTK</span></span>                     | <span data-ttu-id="72ccc-117">text</span><span class="sxs-lookup"><span data-stu-id="72ccc-117">text</span></span>    | <span data-ttu-id="72ccc-118">Y</span><span class="sxs-lookup"><span data-stu-id="72ccc-118">Y</span></span>   | <span data-ttu-id="72ccc-119">N</span><span class="sxs-lookup"><span data-stu-id="72ccc-119">N</span></span>        |
| <span data-ttu-id="72ccc-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="72ccc-120">SymbolPaths</span></span>             | <span data-ttu-id="72ccc-121">text</span><span class="sxs-lookup"><span data-stu-id="72ccc-121">text</span></span>    |     | <span data-ttu-id="72ccc-122">Y</span><span class="sxs-lookup"><span data-stu-id="72ccc-122">Y</span></span>        |
| <span data-ttu-id="72ccc-123">AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="72ccc-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="72ccc-124">integer</span><span class="sxs-lookup"><span data-stu-id="72ccc-124">integer</span></span> |     | <span data-ttu-id="72ccc-125">Y</span><span class="sxs-lookup"><span data-stu-id="72ccc-125">Y</span></span>        |
| <span data-ttu-id="72ccc-126">IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="72ccc-126">IncludeWholeFile</span></span>        | <span data-ttu-id="72ccc-127">integer</span><span class="sxs-lookup"><span data-stu-id="72ccc-127">integer</span></span> |     | <span data-ttu-id="72ccc-128">Y</span><span class="sxs-lookup"><span data-stu-id="72ccc-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="72ccc-129">Columnas</span><span class="sxs-lookup"><span data-stu-id="72ccc-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="72ccc-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado</span><span class="sxs-lookup"><span data-stu-id="72ccc-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="72ccc-131">Clave externa para la columna actualizada de la [tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="72ccc-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="72ccc-132"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="72ccc-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="72ccc-133">Clave de la tabla de archivos.</span><span class="sxs-lookup"><span data-stu-id="72ccc-133">File table key.</span></span> <span data-ttu-id="72ccc-134">Clave externa en la [tabla de archivos](file-table.md) del archivo. msi de la imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="72ccc-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="72ccc-135">Si dos o más imágenes actualizadas dentro de una familia tienen el mismo valor de FTK, el valor debe hacer referencia al mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="72ccc-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="72ccc-136">Los archivos compartidos por varias imágenes de actualización deben tener el mismo FTK para minimizar el tamaño del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="72ccc-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="72ccc-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="72ccc-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="72ccc-138">El valor de este campo se agrega a la lista de carpetas delimitada por signos de punto y coma en la columna SymbolPaths de la [tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) cuando se genera la revisión, y se puede usar para agregar archivos de símbolos para un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="72ccc-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="72ccc-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="72ccc-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="72ccc-140">Establézcalo en 1 para indicar que la revisión no es fundamental.</span><span class="sxs-lookup"><span data-stu-id="72ccc-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="72ccc-141">Establézcalo en 0 para indicar que la revisión es fundamental.</span><span class="sxs-lookup"><span data-stu-id="72ccc-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="72ccc-142">Si Windows Installer encuentra un problema al aplicar esta revisión al archivo especificado en la columna FTK, el valor de este campo determinará si el cuadro de mensaje de error incluye un botón **omitir** para permitir que el usuario continúe el proceso de aplicación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="72ccc-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="72ccc-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="72ccc-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="72ccc-144">Establezca en un valor distinto de cero si se debe instalar el archivo completo especificado en la columna FTK en lugar de crear una revisión binaria.</span><span class="sxs-lookup"><span data-stu-id="72ccc-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 



