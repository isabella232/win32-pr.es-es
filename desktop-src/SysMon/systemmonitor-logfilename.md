---
title: Propiedad SystemMonitor. LogFileName
description: Recupera o establece el nombre de un archivo de registro que se va a utilizar como origen de los valores de contador mostrados en el monitor de sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propiedad nombreDeArchivoDeRegistro SysMon
- Propiedad nombreDeArchivoDeRegistro SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad nombreDeArchivoDeRegistro
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422336"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="dd719-106">Propiedad SystemMonitor. LogFileName</span><span class="sxs-lookup"><span data-stu-id="dd719-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="dd719-107">Recupera o establece el nombre de un archivo de registro que se va a utilizar como origen de los valores de contador mostrados en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="dd719-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="dd719-108">Esta propiedad ha quedado obsoleta en la propiedad [**logfiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="dd719-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="dd719-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd719-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd719-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd719-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="dd719-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dd719-111">Property value</span></span>

<span data-ttu-id="dd719-112">Ruta de acceso al archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="dd719-112">Path to the log file.</span></span> <span data-ttu-id="dd719-113">Puede especificar una ruta de acceso absoluta, relativa o UNC.</span><span class="sxs-lookup"><span data-stu-id="dd719-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="dd719-114">La extensión de nombre de archivo de registro debe ser. csv,. TSV o. BLG.</span><span class="sxs-lookup"><span data-stu-id="dd719-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="dd719-115">Excepciones</span><span class="sxs-lookup"><span data-stu-id="dd719-115">Exceptions</span></span>



| <span data-ttu-id="dd719-116">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="dd719-116">Exception type</span></span>                                  | <span data-ttu-id="dd719-117">Condición</span><span class="sxs-lookup"><span data-stu-id="dd719-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dd719-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="dd719-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="dd719-119">No se puede encontrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="dd719-119">Unable to find the specified file.</span></span> <span data-ttu-id="dd719-120">El valor de Err. number es 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="dd719-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="dd719-121">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="dd719-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="dd719-122">No se puede especificar una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="dd719-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="dd719-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd719-123">Remarks</span></span>

<span data-ttu-id="dd719-124">Esta propiedad devuelve el nombre del archivo de registro del primer miembro de la colección [**logfiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="dd719-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="dd719-125">Si se establece esta propiedad, se producirá un error si la colección [**logfiles**](systemmonitor-logfiles.md) contiene uno o más miembros.</span><span class="sxs-lookup"><span data-stu-id="dd719-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="dd719-126">Debe usar la herramienta Logman.exe o el complemento MMC Perfmon. msc para generar los archivos de registro que se agregan a esta colección.</span><span class="sxs-lookup"><span data-stu-id="dd719-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="dd719-127">En el caso de Perfmon. msc, los registros de contador se encuentran en **registros y alertas de rendimiento**.</span><span class="sxs-lookup"><span data-stu-id="dd719-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="dd719-128">Para obtener información detallada sobre el uso de Logman.exe o Perfmon. msc, busque Logman o use performance, respectivamente, en el **centro de ayuda y soporte técnico**.</span><span class="sxs-lookup"><span data-stu-id="dd719-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd719-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd719-129">Requirements</span></span>



| <span data-ttu-id="dd719-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd719-130">Requirement</span></span> | <span data-ttu-id="dd719-131">Value</span><span class="sxs-lookup"><span data-stu-id="dd719-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd719-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd719-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dd719-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd719-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="dd719-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd719-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dd719-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd719-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd719-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd719-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd719-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="dd719-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd719-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd719-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd719-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="dd719-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="dd719-140">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="dd719-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





