---
description: La tabla ODBCAttribute contiene información sobre los atributos de los controladores y traductores ODBC (Conectividad abierta de bases de datos).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabla ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155132"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="ae013-103">Tabla ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="ae013-103">ODBCAttribute Table</span></span>

<span data-ttu-id="ae013-104">La tabla ODBCAttribute contiene información sobre los atributos de los controladores y traductores ODBC (Conectividad abierta de bases de datos).</span><span class="sxs-lookup"><span data-stu-id="ae013-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="ae013-105">La tabla ODBCAttribute tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae013-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="ae013-106">Columna</span><span class="sxs-lookup"><span data-stu-id="ae013-106">Column</span></span>    | <span data-ttu-id="ae013-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae013-107">Type</span></span>                         | <span data-ttu-id="ae013-108">Clave</span><span class="sxs-lookup"><span data-stu-id="ae013-108">Key</span></span> | <span data-ttu-id="ae013-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ae013-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ae013-110">Controlador\_</span><span class="sxs-lookup"><span data-stu-id="ae013-110">Driver\_</span></span>  | [<span data-ttu-id="ae013-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="ae013-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ae013-112">Y</span><span class="sxs-lookup"><span data-stu-id="ae013-112">Y</span></span>   | <span data-ttu-id="ae013-113">N</span><span class="sxs-lookup"><span data-stu-id="ae013-113">N</span></span>        |
| <span data-ttu-id="ae013-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="ae013-114">Attribute</span></span> | [<span data-ttu-id="ae013-115">Texto</span><span class="sxs-lookup"><span data-stu-id="ae013-115">Text</span></span>](text.md)             | <span data-ttu-id="ae013-116">Y</span><span class="sxs-lookup"><span data-stu-id="ae013-116">Y</span></span>   | <span data-ttu-id="ae013-117">N</span><span class="sxs-lookup"><span data-stu-id="ae013-117">N</span></span>        |
| <span data-ttu-id="ae013-118">Value</span><span class="sxs-lookup"><span data-stu-id="ae013-118">Value</span></span>     | [<span data-ttu-id="ae013-119">Formatea</span><span class="sxs-lookup"><span data-stu-id="ae013-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ae013-120">N</span><span class="sxs-lookup"><span data-stu-id="ae013-120">N</span></span>   | <span data-ttu-id="ae013-121">Y</span><span class="sxs-lookup"><span data-stu-id="ae013-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ae013-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="ae013-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ae013-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Dispositivo\_</span><span class="sxs-lookup"><span data-stu-id="ae013-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="ae013-124">Nombre del token interno para un controlador.</span><span class="sxs-lookup"><span data-stu-id="ae013-124">Internal token name for a driver.</span></span> <span data-ttu-id="ae013-125">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ae013-125">A primary key for the table.</span></span> <span data-ttu-id="ae013-126">Una clave externa en la [tabla ODBCDriver](odbcdriver-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae013-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae013-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui</span><span class="sxs-lookup"><span data-stu-id="ae013-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="ae013-128">Nombre del atributo de controlador.</span><span class="sxs-lookup"><span data-stu-id="ae013-128">Name of the driver attribute.</span></span> <span data-ttu-id="ae013-129">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ae013-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="ae013-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="ae013-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="ae013-131">Valor de cadena localizable para el atributo.</span><span class="sxs-lookup"><span data-stu-id="ae013-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae013-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae013-132">Remarks</span></span>

<span data-ttu-id="ae013-133">Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="ae013-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="ae013-134">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae013-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ae013-135">Validación</span><span class="sxs-lookup"><span data-stu-id="ae013-135">Validation</span></span>

<dl>

[<span data-ttu-id="ae013-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="ae013-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ae013-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="ae013-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ae013-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="ae013-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ae013-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="ae013-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



