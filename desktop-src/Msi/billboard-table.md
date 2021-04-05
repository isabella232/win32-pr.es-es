---
description: En la tabla de la cartelera se muestran los controles de la cartelera mostrados en la interfaz de usuario completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabla de la cartelera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001718"
---
# <a name="billboard-table"></a><span data-ttu-id="29133-103">Tabla de la cartelera</span><span class="sxs-lookup"><span data-stu-id="29133-103">Billboard Table</span></span>

<span data-ttu-id="29133-104">En la tabla de la cartelera se muestran los controles de la [cartelera](billboard-control.md) mostrados en la interfaz de usuario completa.</span><span class="sxs-lookup"><span data-stu-id="29133-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="29133-105">La tabla de la cartelera tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="29133-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="29133-106">Columna</span><span class="sxs-lookup"><span data-stu-id="29133-106">Column</span></span>    | <span data-ttu-id="29133-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="29133-107">Type</span></span>                         | <span data-ttu-id="29133-108">Clave</span><span class="sxs-lookup"><span data-stu-id="29133-108">Key</span></span> | <span data-ttu-id="29133-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="29133-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="29133-110">Valla</span><span class="sxs-lookup"><span data-stu-id="29133-110">Billboard</span></span> | [<span data-ttu-id="29133-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="29133-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="29133-112">Y</span><span class="sxs-lookup"><span data-stu-id="29133-112">Y</span></span>   | <span data-ttu-id="29133-113">N</span><span class="sxs-lookup"><span data-stu-id="29133-113">N</span></span>        |
| <span data-ttu-id="29133-114">Característica\_</span><span class="sxs-lookup"><span data-stu-id="29133-114">Feature\_</span></span> | [<span data-ttu-id="29133-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="29133-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="29133-116">N</span><span class="sxs-lookup"><span data-stu-id="29133-116">N</span></span>   | <span data-ttu-id="29133-117">N</span><span class="sxs-lookup"><span data-stu-id="29133-117">N</span></span>        |
| <span data-ttu-id="29133-118">Acción</span><span class="sxs-lookup"><span data-stu-id="29133-118">Action</span></span>    | [<span data-ttu-id="29133-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="29133-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="29133-120">N</span><span class="sxs-lookup"><span data-stu-id="29133-120">N</span></span>   | <span data-ttu-id="29133-121">Y</span><span class="sxs-lookup"><span data-stu-id="29133-121">Y</span></span>        |
| <span data-ttu-id="29133-122">Ordenación</span><span class="sxs-lookup"><span data-stu-id="29133-122">Ordering</span></span>  | [<span data-ttu-id="29133-123">Entero</span><span class="sxs-lookup"><span data-stu-id="29133-123">Integer</span></span>](integer.md)       | <span data-ttu-id="29133-124">N</span><span class="sxs-lookup"><span data-stu-id="29133-124">N</span></span>   | <span data-ttu-id="29133-125">Y</span><span class="sxs-lookup"><span data-stu-id="29133-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="29133-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="29133-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="29133-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Valla</span><span class="sxs-lookup"><span data-stu-id="29133-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="29133-128">Nombre del control de la [cartelera](billboard-control.md).</span><span class="sxs-lookup"><span data-stu-id="29133-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="29133-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="29133-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="29133-130">Una clave externa a la primera columna de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="29133-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="29133-131">La cartelera solo se muestra si se está instalando esta característica.</span><span class="sxs-lookup"><span data-stu-id="29133-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="29133-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="29133-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="29133-133">Nombre de una acción.</span><span class="sxs-lookup"><span data-stu-id="29133-133">The name of an action.</span></span> <span data-ttu-id="29133-134">La cartelera se muestra durante el progreso de los mensajes recibidos de esta acción.</span><span class="sxs-lookup"><span data-stu-id="29133-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="29133-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Pide</span><span class="sxs-lookup"><span data-stu-id="29133-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="29133-136">Si hay más de una cartelera que corresponde a una acción, se muestran en el orden definido por esta columna.</span><span class="sxs-lookup"><span data-stu-id="29133-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="29133-137">Este número no debe ser negativo.</span><span class="sxs-lookup"><span data-stu-id="29133-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="29133-138">Validación</span><span class="sxs-lookup"><span data-stu-id="29133-138">Validation</span></span>

<dl>

[<span data-ttu-id="29133-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="29133-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="29133-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="29133-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="29133-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="29133-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="29133-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="29133-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



