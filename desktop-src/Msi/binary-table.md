---
description: La tabla binaria contiene los datos binarios de elementos tales como mapas de bits, animaciones e iconos. La tabla binaria también se utiliza para almacenar datos para las acciones personalizadas. Vea limitaciones de OLE en secuencias.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabla binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667015"
---
# <a name="binary-table"></a><span data-ttu-id="45fe7-105">Tabla binaria</span><span class="sxs-lookup"><span data-stu-id="45fe7-105">Binary Table</span></span>

<span data-ttu-id="45fe7-106">La tabla binaria contiene los datos binarios de elementos tales como mapas de bits, animaciones e iconos.</span><span class="sxs-lookup"><span data-stu-id="45fe7-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="45fe7-107">La tabla binaria también se utiliza para almacenar datos para las acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="45fe7-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="45fe7-108">Vea [limitaciones de OLE en secuencias](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="45fe7-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="45fe7-109">La tabla binaria tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="45fe7-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="45fe7-110">Columna</span><span class="sxs-lookup"><span data-stu-id="45fe7-110">Column</span></span> | <span data-ttu-id="45fe7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="45fe7-111">Type</span></span>                         | <span data-ttu-id="45fe7-112">Clave</span><span class="sxs-lookup"><span data-stu-id="45fe7-112">Key</span></span> | <span data-ttu-id="45fe7-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="45fe7-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="45fe7-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="45fe7-114">Name</span></span>   | [<span data-ttu-id="45fe7-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="45fe7-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="45fe7-116">Y</span><span class="sxs-lookup"><span data-stu-id="45fe7-116">Y</span></span>   | <span data-ttu-id="45fe7-117">N</span><span class="sxs-lookup"><span data-stu-id="45fe7-117">N</span></span>        |
| <span data-ttu-id="45fe7-118">Datos</span><span class="sxs-lookup"><span data-stu-id="45fe7-118">Data</span></span>   | [<span data-ttu-id="45fe7-119">Binario</span><span class="sxs-lookup"><span data-stu-id="45fe7-119">Binary</span></span>](binary.md)         | <span data-ttu-id="45fe7-120">N</span><span class="sxs-lookup"><span data-stu-id="45fe7-120">N</span></span>   | <span data-ttu-id="45fe7-121">N</span><span class="sxs-lookup"><span data-stu-id="45fe7-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="45fe7-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="45fe7-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="45fe7-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="45fe7-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="45fe7-124">Una clave única que identifica los datos binarios concretos.</span><span class="sxs-lookup"><span data-stu-id="45fe7-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="45fe7-125">Si los datos binarios son para un control, la clave aparece en la columna de texto del control asociado en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="45fe7-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="45fe7-126">Esta clave debe ser única entre todos los controles que requieren datos binarios.</span><span class="sxs-lookup"><span data-stu-id="45fe7-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="45fe7-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="45fe7-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="45fe7-128">Datos binarios sin formato.</span><span class="sxs-lookup"><span data-stu-id="45fe7-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="45fe7-129">Validación</span><span class="sxs-lookup"><span data-stu-id="45fe7-129">Validation</span></span>

<dl>

[<span data-ttu-id="45fe7-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="45fe7-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="45fe7-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="45fe7-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="45fe7-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="45fe7-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="45fe7-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="45fe7-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



