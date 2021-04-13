---
title: Counters. Add (método)
description: Agrega una instancia de un elemento de objeto a la colección.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Agregar método SysMon
- Agregar método SysMon, clase counters
- Counters (clase) SysMon, Add (método)
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489719"
---
# <a name="countersadd-method"></a><span data-ttu-id="f2e67-106">Counters. Add (método)</span><span class="sxs-lookup"><span data-stu-id="f2e67-106">Counters.Add method</span></span>

<span data-ttu-id="f2e67-107">Agrega una instancia de un [**elemento de objeto**](counteritem.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="f2e67-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e67-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2e67-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="f2e67-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2e67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e67-110">*nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2e67-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e67-111">Ruta de acceso al contador.</span><span class="sxs-lookup"><span data-stu-id="f2e67-111">Path to the counter.</span></span> <span data-ttu-id="f2e67-112">La ruta de acceso puede incluir un nombre de equipo y debe incluir un nombre de objeto de rendimiento, un nombre de instancia de objeto si el objeto de rendimiento especificado admite varias instancias y un nombre de contador.</span><span class="sxs-lookup"><span data-stu-id="f2e67-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="f2e67-113">Esta especificación de ruta de acceso no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f2e67-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="f2e67-114">Para obtener más información sobre cómo especificar una ruta de acceso de contador, consulte [especificar una ruta de acceso de contador](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span><span class="sxs-lookup"><span data-stu-id="f2e67-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="f2e67-115">Excepciones</span><span class="sxs-lookup"><span data-stu-id="f2e67-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2e67-116">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="f2e67-116">Exception type</span></span></th>
<th><span data-ttu-id="f2e67-117">Condición</span><span class="sxs-lookup"><span data-stu-id="f2e67-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2e67-118"><strong>System. Runtime. InteropServices. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="f2e67-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="f2e67-119">Puede recibir esta excepción por una de las siguientes razones:</span><span class="sxs-lookup"><span data-stu-id="f2e67-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="f2e67-120">No se encontró el objeto de rendimiento especificado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f2e67-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="f2e67-121">El valor de Err. number es 0xC0000BB8.</span><span class="sxs-lookup"><span data-stu-id="f2e67-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="f2e67-122">No se pudo encontrar el contador especificado.</span><span class="sxs-lookup"><span data-stu-id="f2e67-122">The specified counter could not be found.</span></span> <span data-ttu-id="f2e67-123">El valor de Err. number es 0xC0000BB9.</span><span class="sxs-lookup"><span data-stu-id="f2e67-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f2e67-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2e67-124">Remarks</span></span>

<span data-ttu-id="f2e67-125">Si especifica un contador de caracteres comodín en el parámetro *PathName* , el método **Add** crea un objeto de [**peritem**](counteritem.md) para cada ruta de acceso expandida.</span><span class="sxs-lookup"><span data-stu-id="f2e67-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="f2e67-126">A continuación, el método **Add** devuelve un puntero al primer **objeto** que se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="f2e67-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="f2e67-127">Si el carácter comodín daría como resultado un contador duplicado, el error no se envía y no se crea ningún duplicado.</span><span class="sxs-lookup"><span data-stu-id="f2e67-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="f2e67-128">Si se produce una condición de error antes de que se creen todos los contadores, se genera el error y no se crean los contadores restantes.</span><span class="sxs-lookup"><span data-stu-id="f2e67-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="f2e67-129">No hay ningún límite en el número de contadores que puede Agregar; sin embargo, SYSMON solo creará un gráfico de los primeros 1.024 contadores de la colección.</span><span class="sxs-lookup"><span data-stu-id="f2e67-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="f2e67-130">No hay ningún límite en el número de contadores que SYSMON mostrará en un informe.</span><span class="sxs-lookup"><span data-stu-id="f2e67-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="f2e67-131">Para recibir una notificación cuando se agrega un contador, implemente el evento [OnCounterAdded](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="f2e67-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e67-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e67-132">Requirements</span></span>



| <span data-ttu-id="f2e67-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e67-133">Requirement</span></span> | <span data-ttu-id="f2e67-134">Value</span><span class="sxs-lookup"><span data-stu-id="f2e67-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e67-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e67-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e67-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2e67-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2e67-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e67-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e67-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2e67-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2e67-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2e67-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e67-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f2e67-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e67-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2e67-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e67-142">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="f2e67-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="f2e67-143">**Counters**</span><span class="sxs-lookup"><span data-stu-id="f2e67-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="f2e67-144">**SystemMonitor.BrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="f2e67-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

