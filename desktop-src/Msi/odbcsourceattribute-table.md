---
description: La tabla ODBCSourceAttribute contiene información sobre los atributos de los orígenes de datos.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabla ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541054"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="b5c61-103">Tabla ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="b5c61-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="b5c61-104">La tabla ODBCSourceAttribute contiene información sobre los atributos de los orígenes de datos.</span><span class="sxs-lookup"><span data-stu-id="b5c61-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="b5c61-105">La tabla ODBCSourceAttribute tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5c61-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="b5c61-106">Columna</span><span class="sxs-lookup"><span data-stu-id="b5c61-106">Column</span></span>       | <span data-ttu-id="b5c61-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5c61-107">Type</span></span>                         | <span data-ttu-id="b5c61-108">Clave</span><span class="sxs-lookup"><span data-stu-id="b5c61-108">Key</span></span> | <span data-ttu-id="b5c61-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b5c61-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="b5c61-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="b5c61-110">DataSource\_</span></span> | [<span data-ttu-id="b5c61-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="b5c61-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b5c61-112">Y</span><span class="sxs-lookup"><span data-stu-id="b5c61-112">Y</span></span>   | <span data-ttu-id="b5c61-113">N</span><span class="sxs-lookup"><span data-stu-id="b5c61-113">N</span></span>        |
| <span data-ttu-id="b5c61-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="b5c61-114">Attribute</span></span>    | [<span data-ttu-id="b5c61-115">Texto</span><span class="sxs-lookup"><span data-stu-id="b5c61-115">Text</span></span>](text.md)             | <span data-ttu-id="b5c61-116">Y</span><span class="sxs-lookup"><span data-stu-id="b5c61-116">Y</span></span>   | <span data-ttu-id="b5c61-117">N</span><span class="sxs-lookup"><span data-stu-id="b5c61-117">N</span></span>        |
| <span data-ttu-id="b5c61-118">Value</span><span class="sxs-lookup"><span data-stu-id="b5c61-118">Value</span></span>        | [<span data-ttu-id="b5c61-119">Formatea</span><span class="sxs-lookup"><span data-stu-id="b5c61-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b5c61-120">N</span><span class="sxs-lookup"><span data-stu-id="b5c61-120">N</span></span>   | <span data-ttu-id="b5c61-121">Y</span><span class="sxs-lookup"><span data-stu-id="b5c61-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b5c61-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="b5c61-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b5c61-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span><span class="sxs-lookup"><span data-stu-id="b5c61-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="b5c61-124">Nombre del token interno para el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="b5c61-124">Internal token name for data source.</span></span> <span data-ttu-id="b5c61-125">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b5c61-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="b5c61-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui</span><span class="sxs-lookup"><span data-stu-id="b5c61-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="b5c61-127">Nombre del atributo de origen de datos.</span><span class="sxs-lookup"><span data-stu-id="b5c61-127">Name of data source attribute.</span></span> <span data-ttu-id="b5c61-128">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b5c61-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="b5c61-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="b5c61-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="b5c61-130">Valor de cadena traducible para el atributo.</span><span class="sxs-lookup"><span data-stu-id="b5c61-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5c61-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5c61-131">Remarks</span></span>

<span data-ttu-id="b5c61-132">Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="b5c61-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="b5c61-133">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5c61-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b5c61-134">Validación</span><span class="sxs-lookup"><span data-stu-id="b5c61-134">Validation</span></span>

<dl>

[<span data-ttu-id="b5c61-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="b5c61-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b5c61-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="b5c61-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b5c61-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="b5c61-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b5c61-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="b5c61-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



