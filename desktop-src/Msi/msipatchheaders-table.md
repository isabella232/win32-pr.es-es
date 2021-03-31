---
description: La tabla MsiPatchHeaders contiene las secuencias de encabezado de la revisión binaria que se usan para la validación de revisiones.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabla MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277165"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="8db1f-103">Tabla MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="8db1f-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="8db1f-104">La tabla MsiPatchHeaders contiene las secuencias de encabezado de la revisión binaria que se usan para la validación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="8db1f-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="8db1f-105">La tabla MsiPatchHeaders se utiliza cuando las claves de [tabla de archivos](file-table.md) largas producen un error al generar la secuencia de encabezado patch en la [tabla patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="8db1f-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="8db1f-106">Esto puede deberse a la limitación del nombre de flujo que se describe en [limitaciones OLE en secuencias](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="8db1f-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="8db1f-107">En este caso, la tabla patch puede hacer referencia a la tabla MsiPatchHeaders para crear la secuencia de encabezado patch.</span><span class="sxs-lookup"><span data-stu-id="8db1f-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="8db1f-108">La tabla MsiPatchHeaders tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="8db1f-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="8db1f-109">Columna</span><span class="sxs-lookup"><span data-stu-id="8db1f-109">Column</span></span>    | <span data-ttu-id="8db1f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8db1f-110">Type</span></span>                         | <span data-ttu-id="8db1f-111">Clave</span><span class="sxs-lookup"><span data-stu-id="8db1f-111">Key</span></span> | <span data-ttu-id="8db1f-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="8db1f-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="8db1f-113">StreamRef</span><span class="sxs-lookup"><span data-stu-id="8db1f-113">StreamRef</span></span> | [<span data-ttu-id="8db1f-114">Identificador</span><span class="sxs-lookup"><span data-stu-id="8db1f-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="8db1f-115">Y</span><span class="sxs-lookup"><span data-stu-id="8db1f-115">Y</span></span>   | <span data-ttu-id="8db1f-116">N</span><span class="sxs-lookup"><span data-stu-id="8db1f-116">N</span></span>        |
| <span data-ttu-id="8db1f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8db1f-117">Header</span></span>    | [<span data-ttu-id="8db1f-118">Binario</span><span class="sxs-lookup"><span data-stu-id="8db1f-118">Binary</span></span>](binary.md)         | <span data-ttu-id="8db1f-119">N</span><span class="sxs-lookup"><span data-stu-id="8db1f-119">N</span></span>   | <span data-ttu-id="8db1f-120">N</span><span class="sxs-lookup"><span data-stu-id="8db1f-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8db1f-121">Columnas</span><span class="sxs-lookup"><span data-stu-id="8db1f-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8db1f-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span><span class="sxs-lookup"><span data-stu-id="8db1f-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="8db1f-123">La clave principal de la tabla que identifica de forma única un encabezado patch determinado.</span><span class="sxs-lookup"><span data-stu-id="8db1f-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="8db1f-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Encabezado</span><span class="sxs-lookup"><span data-stu-id="8db1f-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="8db1f-125">Esta columna es el encabezado de revisión de la secuencia binaria que se utiliza para la validación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="8db1f-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8db1f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8db1f-126">Remarks</span></span>

<span data-ttu-id="8db1f-127">La [acción PatchFiles](patchfiles-action.md)procesa esta tabla.</span><span class="sxs-lookup"><span data-stu-id="8db1f-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="8db1f-128">Esta tabla normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="8db1f-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="8db1f-129">Normalmente no se crea directamente en un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="8db1f-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="8db1f-130">Validación</span><span class="sxs-lookup"><span data-stu-id="8db1f-130">Validation</span></span>

<dl>

[<span data-ttu-id="8db1f-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="8db1f-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8db1f-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="8db1f-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8db1f-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="8db1f-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



