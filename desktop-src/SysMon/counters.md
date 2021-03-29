---
title: Colección counters (Isysmon. h)
description: Utilice esta clase para administrar la colección de objetos de tipo de elemento. Para recuperar este objeto, llame a SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Colección de contadores SysMon
- Colección de contadores SysMon, descripción
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666048"
---
# <a name="counters-collection"></a><span data-ttu-id="cbd1e-106">Colección de contadores</span><span class="sxs-lookup"><span data-stu-id="cbd1e-106">Counters collection</span></span>

<span data-ttu-id="cbd1e-107">Utilice esta clase para administrar la colección de objetos de tipo de [**elemento**](counteritem.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd1e-107">Use this class to manage the collection of [**CounterItem**](counteritem.md) objects.</span></span>

<span data-ttu-id="cbd1e-108">Para recuperar este objeto, llame a [**SystemMonitor. counters**](systemmonitor-counters.md).</span><span class="sxs-lookup"><span data-stu-id="cbd1e-108">To retrieve this object, call [**SystemMonitor.Counters**](systemmonitor-counters.md).</span></span>

## <a name="members"></a><span data-ttu-id="cbd1e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cbd1e-109">Members</span></span>

<span data-ttu-id="cbd1e-110">La colección **counters** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cbd1e-110">The **Counters** collection has these types of members:</span></span>

-   [<span data-ttu-id="cbd1e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cbd1e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cbd1e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbd1e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cbd1e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cbd1e-113">Methods</span></span>

<span data-ttu-id="cbd1e-114">La colección **counters** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-114">The **Counters** collection has these methods.</span></span>



| <span data-ttu-id="cbd1e-115">Método</span><span class="sxs-lookup"><span data-stu-id="cbd1e-115">Method</span></span>                            | <span data-ttu-id="cbd1e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbd1e-116">Description</span></span>                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbd1e-117">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="cbd1e-117">**Add**</span></span>](counters-add.md)       | <span data-ttu-id="cbd1e-118">Agrega una instancia de un [**elemento de objeto**](counteritem.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-118">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="cbd1e-119">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="cbd1e-119">**Remove**</span></span>](counters-remove.md) | <span data-ttu-id="cbd1e-120">Quita una instancia de un [**objeto**](counteritem.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-120">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cbd1e-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbd1e-121">Properties</span></span>

<span data-ttu-id="cbd1e-122">La colección **counters** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-122">The **Counters** collection has these properties.</span></span>



| <span data-ttu-id="cbd1e-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbd1e-123">Property</span></span>                                   | <span data-ttu-id="cbd1e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbd1e-124">Description</span></span>                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbd1e-125">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="cbd1e-125">**Count**</span></span>](counters-count.md)<br/> | <span data-ttu-id="cbd1e-126">Recupera el número de instancias de los [**Contraelementos**](counteritem.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-126">Retrieves the number of [**CounterItem**](counteritem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="cbd1e-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cbd1e-127">**Item**</span></span>](counters-item.md)<br/>   | <span data-ttu-id="cbd1e-128">Recupera la instancia de un [**elemento de objeto**](counteritem.md) especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-128">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbd1e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbd1e-129">Remarks</span></span>

<span data-ttu-id="cbd1e-130">El objeto **counters** es la propiedad predeterminada del objeto [**SystemMonitor**](systemmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd1e-130">The **Counters** object is the default property of the [**SystemMonitor**](systemmonitor.md) object.</span></span>

<span data-ttu-id="cbd1e-131">Agregue a esta colección los contadores que desea representar en un gráfico.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-131">Add to this collection those counters that you want to graph.</span></span> <span data-ttu-id="cbd1e-132">SYSMON recupera los valores del contador desde el sistema o desde un archivo de registro, en función del [**origen de datos**](systemmonitor-datasourcetype.md) que especifique.</span><span class="sxs-lookup"><span data-stu-id="cbd1e-132">SYSMON retrieves the counter values either from the system or from a log file depending on the [**data source**](systemmonitor-datasourcetype.md) that you specify.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd1e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbd1e-133">Requirements</span></span>



| <span data-ttu-id="cbd1e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd1e-134">Requirement</span></span> | <span data-ttu-id="cbd1e-135">Value</span><span class="sxs-lookup"><span data-stu-id="cbd1e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd1e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbd1e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd1e-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cbd1e-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cbd1e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbd1e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd1e-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cbd1e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cbd1e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbd1e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbd1e-141"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbd1e-141"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cbd1e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbd1e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbd1e-143"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cbd1e-143"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





