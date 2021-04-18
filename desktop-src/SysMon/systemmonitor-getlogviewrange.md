---
title: SystemMonitor. GetLogViewRange, método
description: Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Método GetLogViewRange SysMon
- Método GetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534185"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="3ae6c-106">SystemMonitor. GetLogViewRange, método</span><span class="sxs-lookup"><span data-stu-id="3ae6c-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="3ae6c-107">Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="3ae6c-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae6c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ae6c-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="3ae6c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ae6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae6c-110">*StartTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3ae6c-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae6c-111">Fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="3ae6c-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="3ae6c-112">*StopTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3ae6c-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae6c-113">Fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="3ae6c-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae6c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ae6c-114">Return value</span></span>

<span data-ttu-id="3ae6c-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3ae6c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ae6c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ae6c-116">Remarks</span></span>

<span data-ttu-id="3ae6c-117">SYSMON recupera los valores de los contadores de los archivos de registro que se encuentran dentro de las fechas de inicio y de finalización, en su interior.</span><span class="sxs-lookup"><span data-stu-id="3ae6c-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="3ae6c-118">El uso de este método es igual que el acceso a las propiedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae6c-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae6c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ae6c-119">Requirements</span></span>



| <span data-ttu-id="3ae6c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae6c-120">Requirement</span></span> | <span data-ttu-id="3ae6c-121">Value</span><span class="sxs-lookup"><span data-stu-id="3ae6c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae6c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae6c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae6c-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae6c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ae6c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae6c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae6c-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae6c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ae6c-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ae6c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae6c-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3ae6c-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae6c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ae6c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae6c-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3ae6c-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="3ae6c-130">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="3ae6c-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





