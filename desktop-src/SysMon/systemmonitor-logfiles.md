---
title: Propiedad SystemMonitor. LogFiles
description: Colección de uno o más archivos de registro que se van a utilizar como origen de los valores de contador mostrados en el monitor de sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propiedad logfiles SysMon
- Propiedad logfiles SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad logfiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665985"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="3085c-106">Propiedad SystemMonitor. LogFiles</span><span class="sxs-lookup"><span data-stu-id="3085c-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="3085c-107">Colección de uno o más archivos de registro que se van a utilizar como origen de los valores de contador mostrados en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="3085c-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="3085c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3085c-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="3085c-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3085c-109">Property value</span></span>

<span data-ttu-id="3085c-110">Colección de objetos [**LogFileItem**](logfileitem.md) que especifican los archivos de registro que se usan como origen de datos para el gráfico.</span><span class="sxs-lookup"><span data-stu-id="3085c-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="3085c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3085c-111">Remarks</span></span>

<span data-ttu-id="3085c-112">Para agregar o quitar un archivo de registro de la colección de archivos de registro, el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) no debe estar establecido en sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="3085c-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="3085c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3085c-113">Requirements</span></span>



| <span data-ttu-id="3085c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3085c-114">Requirement</span></span> | <span data-ttu-id="3085c-115">Value</span><span class="sxs-lookup"><span data-stu-id="3085c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3085c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3085c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3085c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3085c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3085c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3085c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3085c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3085c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3085c-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3085c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3085c-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3085c-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3085c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3085c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3085c-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3085c-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="3085c-124">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="3085c-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="3085c-125">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="3085c-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="3085c-126">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="3085c-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="3085c-127">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="3085c-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





