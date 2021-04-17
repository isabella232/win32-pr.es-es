---
description: La tabla FileSFPCatalog asocia los archivos especificados con los archivos de catálogo usados por la protección de archivos del sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabla FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668070"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="3f03b-103">Tabla FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="3f03b-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="3f03b-104">La tabla FileSFPCatalog asocia los archivos especificados con los archivos de catálogo usados por la protección de archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f03b-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="3f03b-105">**Windows Vista, Windows Server 2003 y Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="3f03b-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="3f03b-106">La tabla FileSFPCatalog tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="3f03b-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="3f03b-107">Columna</span><span class="sxs-lookup"><span data-stu-id="3f03b-107">Column</span></span>       | <span data-ttu-id="3f03b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f03b-108">Type</span></span>                         | <span data-ttu-id="3f03b-109">Clave</span><span class="sxs-lookup"><span data-stu-id="3f03b-109">Key</span></span> | <span data-ttu-id="3f03b-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="3f03b-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="3f03b-111">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="3f03b-111">File\_</span></span>       | [<span data-ttu-id="3f03b-112">Identificador</span><span class="sxs-lookup"><span data-stu-id="3f03b-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="3f03b-113">Y</span><span class="sxs-lookup"><span data-stu-id="3f03b-113">Y</span></span>   | <span data-ttu-id="3f03b-114">N</span><span class="sxs-lookup"><span data-stu-id="3f03b-114">N</span></span>        |
| <span data-ttu-id="3f03b-115">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="3f03b-115">SFPCatalog\_</span></span> | [<span data-ttu-id="3f03b-116">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="3f03b-116">Filename</span></span>](filename.md)     | <span data-ttu-id="3f03b-117">Y</span><span class="sxs-lookup"><span data-stu-id="3f03b-117">Y</span></span>   | <span data-ttu-id="3f03b-118">N</span><span class="sxs-lookup"><span data-stu-id="3f03b-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3f03b-119">Columnas</span><span class="sxs-lookup"><span data-stu-id="3f03b-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3f03b-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="3f03b-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="3f03b-121">Clave externa de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f03b-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f03b-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="3f03b-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="3f03b-123">Clave externa para la [tabla SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f03b-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f03b-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f03b-124">Remarks</span></span>

<span data-ttu-id="3f03b-125">La [acción InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta la tabla de [componentes](component-table.md), la tabla de [archivos](file-table.md), la tabla FileSFPCatalog y la tabla [SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f03b-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="3f03b-126">Validación</span><span class="sxs-lookup"><span data-stu-id="3f03b-126">Validation</span></span>

<dl>

[<span data-ttu-id="3f03b-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="3f03b-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3f03b-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="3f03b-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3f03b-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="3f03b-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3f03b-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="3f03b-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="3f03b-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="3f03b-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



