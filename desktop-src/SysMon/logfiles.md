---
title: Objeto LogFiles (Isysmon.h)
description: Utilice esta clase para administrar una colección de uno o varios archivos de registro que contengan datos del contador de rendimiento. Para recuperar este objeto, llame a SystemMonitor. logfiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- LogFiles (objeto) SysMon
- LogFiles (objeto) SysMon, descrito
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488944"
---
# <a name="logfiles-object"></a><span data-ttu-id="ce72e-105">LogFiles (objeto)</span><span class="sxs-lookup"><span data-stu-id="ce72e-105">LogFiles object</span></span>

<span data-ttu-id="ce72e-106">Utilice esta clase para administrar una colección de uno o varios archivos de registro que contengan datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ce72e-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="ce72e-107">Para recuperar este objeto, llame a [**SystemMonitor. logfiles**](systemmonitor-logfiles.md).</span><span class="sxs-lookup"><span data-stu-id="ce72e-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="ce72e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce72e-108">Members</span></span>

<span data-ttu-id="ce72e-109">El objeto **logfiles** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ce72e-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="ce72e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce72e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ce72e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce72e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ce72e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce72e-112">Methods</span></span>

<span data-ttu-id="ce72e-113">El objeto **logfiles** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ce72e-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="ce72e-114">Método</span><span class="sxs-lookup"><span data-stu-id="ce72e-114">Method</span></span>                                          | <span data-ttu-id="ce72e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce72e-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce72e-116">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="ce72e-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="ce72e-117">Agrega una instancia de [**LogFileItem**](logfileitem.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="ce72e-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="ce72e-118">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="ce72e-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="ce72e-119">Quita una instancia de [**LogFileItem**](logfileitem.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="ce72e-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ce72e-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce72e-120">Properties</span></span>

<span data-ttu-id="ce72e-121">El objeto **logfiles** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce72e-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="ce72e-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce72e-122">Property</span></span>                                                 | <span data-ttu-id="ce72e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce72e-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce72e-124">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="ce72e-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="ce72e-125">Recupera el número de instancias de [**LogFileItem**](logfileitem.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="ce72e-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="ce72e-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce72e-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="ce72e-127">Recupera la instancia de [**LogFileItem**](logfileitem.md) especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="ce72e-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce72e-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce72e-128">Remarks</span></span>

<span data-ttu-id="ce72e-129">Para que SYSMON muestre los contadores de rendimiento de un archivo de registro, establezca [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) en [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="ce72e-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="ce72e-130">Después de agregar los archivos de registro a la colección, utilice la colección [**counters**](counters.md) para especificar los datos de los contadores que desea leer de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="ce72e-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="ce72e-131">Tenga en cuenta que si **SystemMonitor. DataSourceType** está establecido en **DataSourceTypeConstants.sysmonLogFiles**, SYSMON volverá a muestrear los archivos de registro cada vez que agregue un archivo de registro o un contador a sus respectivas colecciones.</span><span class="sxs-lookup"><span data-stu-id="ce72e-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="ce72e-132">**Antes de Windows Vista:** No puede Agregar archivos de registro a la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="ce72e-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="ce72e-133">En primer lugar, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonNullDataSource**, agregue los archivos de registro y los contadores y, a continuación, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="ce72e-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="ce72e-134">Las propiedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) especifican el intervalo de valores muestreados de los archivos de registro a Graph.</span><span class="sxs-lookup"><span data-stu-id="ce72e-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="ce72e-135">SYSMON los gráficos solo representan los datos del archivo de registro (la vista de gráfico no se desplaza como lo hace al representar gráficamente la actividad actual del equipo).</span><span class="sxs-lookup"><span data-stu-id="ce72e-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="ce72e-136">Si los datos muestreados superan lo que se puede mostrar en una sola vista de gráfico, SYSMON comprime los datos muestreados (cada punto en el gráfico representa el promedio de varios valores muestreados) para ajustar todos los datos muestreados de los archivos de registro del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ce72e-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce72e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce72e-137">Requirements</span></span>



| <span data-ttu-id="ce72e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce72e-138">Requirement</span></span> | <span data-ttu-id="ce72e-139">Value</span><span class="sxs-lookup"><span data-stu-id="ce72e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce72e-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce72e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ce72e-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ce72e-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ce72e-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce72e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ce72e-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce72e-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce72e-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce72e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce72e-145"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce72e-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ce72e-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce72e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce72e-147"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ce72e-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





