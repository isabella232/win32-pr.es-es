---
description: MsiFiler.exe rellena la tabla de archivos con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la tabla MsiFileHash con los hash de archivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666464"
---
# <a name="msifilerexe"></a><span data-ttu-id="fb9ed-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="fb9ed-104">Msifiler.exe</span></span>

<span data-ttu-id="fb9ed-105">MsiFiler.exe rellena la [tabla de archivos](file-table.md) con versiones de archivo, idiomas y tamaños basados en un directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="fb9ed-106">También puede actualizar la [tabla MsiFileHash](msifilehash-table.md) con los hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9ed-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb9ed-107">Syntax</span></span>

<span data-ttu-id="fb9ed-108">**msifiler.exe-d** *{base de datos}* **\[ -v- \] \[ h \] \[ - \] s ALTSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fb9ed-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="fb9ed-109">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="fb9ed-109">Command Line Options</span></span>

<span data-ttu-id="fb9ed-110">Msifiler.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="fb9ed-111">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="fb9ed-112">Opción</span><span class="sxs-lookup"><span data-stu-id="fb9ed-112">Option</span></span> | <span data-ttu-id="fb9ed-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fb9ed-113">Parameter</span></span>   | <span data-ttu-id="fb9ed-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb9ed-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9ed-115">-d</span><span class="sxs-lookup"><span data-stu-id="fb9ed-115">-d</span></span>     | <span data-ttu-id="fb9ed-116">*database*</span><span class="sxs-lookup"><span data-stu-id="fb9ed-116">*database*</span></span>  | <span data-ttu-id="fb9ed-117">La base de datos (archivo. msi) que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="fb9ed-118">-v</span><span class="sxs-lookup"><span data-stu-id="fb9ed-118">-v</span></span>     |             | <span data-ttu-id="fb9ed-119">Usar el modo detallado.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="fb9ed-120">-H</span><span class="sxs-lookup"><span data-stu-id="fb9ed-120">-h</span></span>     |             | <span data-ttu-id="fb9ed-121">Rellene la [tabla MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb9ed-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="fb9ed-122">Esto crea la tabla si aún no existe.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="fb9ed-123">La tabla MsiFileHash solo se puede usar con archivos sin versión.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="fb9ed-124">-S</span><span class="sxs-lookup"><span data-stu-id="fb9ed-124">-s</span></span>     | <span data-ttu-id="fb9ed-125">*ALTSOURCE*</span><span class="sxs-lookup"><span data-stu-id="fb9ed-125">*ALTSOURCE*</span></span> | <span data-ttu-id="fb9ed-126">ALTSOURCE especifica un directorio alternativo para encontrar los archivos.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="fb9ed-127">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="fb9ed-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb9ed-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb9ed-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb9ed-129">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fb9ed-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="fb9ed-130">Usar la tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="fb9ed-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="fb9ed-131">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="fb9ed-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



