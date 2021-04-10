---
title: Propiedad SystemMonitor. DataPointCount
description: Recupera o establece el número de puntos de datos mostrados en un gráfico de líneas.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propiedad DataPointCount SysMon
- Propiedad DataPointCount SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996163"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="c53c6-106">Propiedad SystemMonitor. DataPointCount</span><span class="sxs-lookup"><span data-stu-id="c53c6-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="c53c6-107">Recupera o establece el número de puntos de datos mostrados en un gráfico de líneas.</span><span class="sxs-lookup"><span data-stu-id="c53c6-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="c53c6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c53c6-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="c53c6-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c53c6-109">Property value</span></span>

<span data-ttu-id="c53c6-110">Número de puntos de datos mostrados en la vista de un gráfico de líneas.</span><span class="sxs-lookup"><span data-stu-id="c53c6-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="c53c6-111">El valor predeterminado es 100 puntos de datos.</span><span class="sxs-lookup"><span data-stu-id="c53c6-111">The default value is 100 data points.</span></span> <span data-ttu-id="c53c6-112">El intervalo válido de valores es de 2 a 1.000.</span><span class="sxs-lookup"><span data-stu-id="c53c6-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="c53c6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c53c6-113">Remarks</span></span>

<span data-ttu-id="c53c6-114">Esta propiedad solo se usa si [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) es **sysmonCurrentActivity**.</span><span class="sxs-lookup"><span data-stu-id="c53c6-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c53c6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c53c6-115">Requirements</span></span>



| <span data-ttu-id="c53c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c53c6-116">Requirement</span></span> | <span data-ttu-id="c53c6-117">Value</span><span class="sxs-lookup"><span data-stu-id="c53c6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c53c6-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c53c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c53c6-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c53c6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c53c6-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c53c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c53c6-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c53c6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c53c6-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c53c6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c53c6-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c53c6-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





