---
title: Método GetDataAt
description: Recupera el valor del contador especificado de un punto concreto del gráfico.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Método GetDataAt SysMon
- Método GetDataAt SysMon, objeto de contraelemento
- Objeto de contraelemento SysMon, método GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534306"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="8d0dc-106">Método GetDataAt</span><span class="sxs-lookup"><span data-stu-id="8d0dc-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="8d0dc-107">Recupera el valor del contador especificado de un punto concreto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="8d0dc-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0dc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d0dc-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="8d0dc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d0dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d0dc-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8d0dc-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0dc-111">Índice de base cero del punto del gráfico cuyo valor se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="8d0dc-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="8d0dc-112">Los valores válidos van de 0 a ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).</span><span class="sxs-lookup"><span data-stu-id="8d0dc-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="8d0dc-113">*qué* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d0dc-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0dc-114">Tipo de valor de contador que se va a recuperar, por ejemplo, el valor medio del contador tal y como se muestra en la ventana del gráfico.</span><span class="sxs-lookup"><span data-stu-id="8d0dc-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="8d0dc-115">Para obtener los valores posibles, vea [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span><span class="sxs-lookup"><span data-stu-id="8d0dc-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="8d0dc-116">*variante* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d0dc-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0dc-117">Valor del contador que se recuperó.</span><span class="sxs-lookup"><span data-stu-id="8d0dc-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d0dc-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d0dc-118">Return value</span></span>

<span data-ttu-id="8d0dc-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8d0dc-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d0dc-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d0dc-120">Remarks</span></span>

<span data-ttu-id="8d0dc-121">Use este método solo si</span><span class="sxs-lookup"><span data-stu-id="8d0dc-121">Use this method only if</span></span>

-   <span data-ttu-id="8d0dc-122">[**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) está establecido en sysmonLineGraph</span><span class="sxs-lookup"><span data-stu-id="8d0dc-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="8d0dc-123">[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en SysmonLogFiles o sysmonSqlLog</span><span class="sxs-lookup"><span data-stu-id="8d0dc-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0dc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d0dc-124">Requirements</span></span>



| <span data-ttu-id="8d0dc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d0dc-125">Requirement</span></span> | <span data-ttu-id="8d0dc-126">Value</span><span class="sxs-lookup"><span data-stu-id="8d0dc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0dc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d0dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8d0dc-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d0dc-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d0dc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d0dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8d0dc-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d0dc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d0dc-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d0dc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d0dc-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8d0dc-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d0dc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d0dc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d0dc-134">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="8d0dc-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="8d0dc-135">**Elemento de GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="8d0dc-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="8d0dc-136">**Peritem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="8d0dc-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





