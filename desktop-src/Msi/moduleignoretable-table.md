---
description: Si una tabla del módulo de combinación aparece en la tabla ModuleIgnoreTable, no se combina en el archivo. msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabla ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278810"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="026b9-103">Tabla ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="026b9-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="026b9-104">Si una tabla del módulo de combinación aparece en la tabla ModuleIgnoreTable, no se combina en el archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="026b9-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="026b9-105">Si la tabla ya existe en el archivo. msi, la combinación no la modifica.</span><span class="sxs-lookup"><span data-stu-id="026b9-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="026b9-106">Por tanto, las tablas de ModuleIgnoreTable pueden contener datos innecesarios después de la combinación.</span><span class="sxs-lookup"><span data-stu-id="026b9-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="026b9-107">La tabla ModuleIgnoreTable tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="026b9-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="026b9-108">Columna</span><span class="sxs-lookup"><span data-stu-id="026b9-108">Column</span></span> | <span data-ttu-id="026b9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="026b9-109">Type</span></span>                         | <span data-ttu-id="026b9-110">Clave</span><span class="sxs-lookup"><span data-stu-id="026b9-110">Key</span></span> | <span data-ttu-id="026b9-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="026b9-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="026b9-112">Tabla</span><span class="sxs-lookup"><span data-stu-id="026b9-112">Table</span></span>  | [<span data-ttu-id="026b9-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="026b9-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="026b9-114">S</span><span class="sxs-lookup"><span data-stu-id="026b9-114">Y</span></span>   | <span data-ttu-id="026b9-115">No</span><span class="sxs-lookup"><span data-stu-id="026b9-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="026b9-116">Columnas</span><span class="sxs-lookup"><span data-stu-id="026b9-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="026b9-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="026b9-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="026b9-118">Nombre de la tabla del módulo de combinación que no se va a combinar en el archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="026b9-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="026b9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="026b9-119">Remarks</span></span>

<span data-ttu-id="026b9-120">Para minimizar el tamaño del archivo. MSM, se recomienda que los desarrolladores quiten las tablas sin usar de los módulos destinados a la redistribución en lugar de enumerar estas tablas en la tabla ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="026b9-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



