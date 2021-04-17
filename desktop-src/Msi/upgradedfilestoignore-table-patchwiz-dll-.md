---
description: La tabla UpgradedFilesToIgnore evita la actualización de archivos específicos que se han modificado en la imagen actualizada con respecto a las imágenes de destino.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabla UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653023"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="10100-103">Tabla UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="10100-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="10100-104">La tabla UpgradedFilesToIgnore evita la actualización de archivos específicos que se han modificado en la imagen actualizada con respecto a las imágenes de destino.</span><span class="sxs-lookup"><span data-stu-id="10100-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="10100-105">Puede ser útil para hacer esto en ciertos casos.</span><span class="sxs-lookup"><span data-stu-id="10100-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="10100-106">Por ejemplo, un paquete de revisión diseñado únicamente para su uso con instalaciones no administrativas no necesita incluir archivos de revisión que solo formen parte de las imágenes administrativas.</span><span class="sxs-lookup"><span data-stu-id="10100-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="10100-107">La exclusión de estos archivos usados únicamente en imágenes administrativas puede reducir el tamaño del paquete de revisión; sin embargo, se debe informar a los administradores sobre cómo actualizar estos archivos por separado.</span><span class="sxs-lookup"><span data-stu-id="10100-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="10100-108">Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="10100-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="10100-109">La tabla UpgradedFilesToIgnore tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="10100-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="10100-110">Columna</span><span class="sxs-lookup"><span data-stu-id="10100-110">Column</span></span>   | <span data-ttu-id="10100-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="10100-111">Type</span></span> | <span data-ttu-id="10100-112">Clave</span><span class="sxs-lookup"><span data-stu-id="10100-112">Key</span></span> | <span data-ttu-id="10100-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="10100-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="10100-114">Upgraded</span><span class="sxs-lookup"><span data-stu-id="10100-114">Upgraded</span></span> | <span data-ttu-id="10100-115">text</span><span class="sxs-lookup"><span data-stu-id="10100-115">text</span></span> | <span data-ttu-id="10100-116">Y</span><span class="sxs-lookup"><span data-stu-id="10100-116">Y</span></span>   | <span data-ttu-id="10100-117">N</span><span class="sxs-lookup"><span data-stu-id="10100-117">N</span></span>        |
| <span data-ttu-id="10100-118">FTK</span><span class="sxs-lookup"><span data-stu-id="10100-118">FTK</span></span>      | <span data-ttu-id="10100-119">text</span><span class="sxs-lookup"><span data-stu-id="10100-119">text</span></span> | <span data-ttu-id="10100-120">Y</span><span class="sxs-lookup"><span data-stu-id="10100-120">Y</span></span>   | <span data-ttu-id="10100-121">N</span><span class="sxs-lookup"><span data-stu-id="10100-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="10100-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="10100-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="10100-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado</span><span class="sxs-lookup"><span data-stu-id="10100-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="10100-124">Clave externa para la columna actualizada de la [tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="10100-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="10100-125">La herramienta de creación de revisiones excluye la actualización del archivo especificado en la columna FTK de la tabla UpgradedFilesToIgnore al actualizar un destino a la imagen especificada en el campo actualizado.</span><span class="sxs-lookup"><span data-stu-id="10100-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="10100-126">Escriba un valor de " \* " en el campo actualizado para excluir la actualización del archivo para todas las imágenes actualizadas.</span><span class="sxs-lookup"><span data-stu-id="10100-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="10100-127"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="10100-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="10100-128">Clave externa en la [tabla de archivos](file-table.md) de la imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="10100-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="10100-129">Un valor de la forma " <prefix> \* " coincide con todas las claves de la tabla de archivos que comienzan con ese prefijo.</span><span class="sxs-lookup"><span data-stu-id="10100-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="10100-130">Ningún texto puede seguir el asterisco.</span><span class="sxs-lookup"><span data-stu-id="10100-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 



