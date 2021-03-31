---
title: Propiedad SystemMonitor. ChartScroll
description: Recupera o establece un valor que determina si el gráfico de líneas se desplaza en la vista.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Propiedad ChartScroll SysMon
- Propiedad ChartScroll SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996494"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="56cdf-106">Propiedad SystemMonitor. ChartScroll</span><span class="sxs-lookup"><span data-stu-id="56cdf-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="56cdf-107">Recupera o establece un valor que determina si el gráfico de líneas se desplaza en la vista.</span><span class="sxs-lookup"><span data-stu-id="56cdf-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cdf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56cdf-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="56cdf-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56cdf-109">Property value</span></span>

<span data-ttu-id="56cdf-110">True si el gráfico de líneas se desplaza continuamente de derecha a izquierda; en caso contrario, false si el gráfico de líneas se dibuja de izquierda a derecha y se ajusta en sí mismo en la vista.</span><span class="sxs-lookup"><span data-stu-id="56cdf-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="56cdf-111">False es la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="56cdf-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="56cdf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56cdf-112">Remarks</span></span>

<span data-ttu-id="56cdf-113">Este valor se omite si [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) no es [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="56cdf-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="56cdf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56cdf-114">Requirements</span></span>



| <span data-ttu-id="56cdf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cdf-115">Requirement</span></span> | <span data-ttu-id="56cdf-116">Value</span><span class="sxs-lookup"><span data-stu-id="56cdf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56cdf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56cdf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56cdf-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56cdf-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56cdf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56cdf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56cdf-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56cdf-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56cdf-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56cdf-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56cdf-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="56cdf-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





