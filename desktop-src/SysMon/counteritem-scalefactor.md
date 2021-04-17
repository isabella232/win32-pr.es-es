---
title: Propiedad ScaleFactor.
description: Recupera o establece el factor de escala que se usa para representar el valor del contador.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propiedad ScaleFactor SysMon
- Propiedad ScaleFactor SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666015"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="b4075-106">Propiedad ScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="b4075-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="b4075-107">Recupera o establece el factor de escala que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="b4075-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="b4075-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b4075-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4075-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4075-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="b4075-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4075-110">Property value</span></span>

<span data-ttu-id="b4075-111">Factor de escala que se usa para mostrar los valores del contador con gráficos.</span><span class="sxs-lookup"><span data-stu-id="b4075-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="b4075-112">Los valores válidos van de-9 a 9 (los valores corresponden a 0,000000001-100000000,0).</span><span class="sxs-lookup"><span data-stu-id="b4075-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="b4075-113">**Antes de Windows Vista:** Los valores válidos van de-7 a 7 (los valores corresponden a 0,0000001-1000000,0).</span><span class="sxs-lookup"><span data-stu-id="b4075-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4075-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4075-114">Remarks</span></span>

<span data-ttu-id="b4075-115">Establezca esta propiedad únicamente si desea cambiar el factor de escala predeterminado del contador (cada contador define su propio factor de escala).</span><span class="sxs-lookup"><span data-stu-id="b4075-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="b4075-116">El valor de esta propiedad se establece en Integer. MaxValue si el contador utiliza su factor de escala predeterminado para representar gráficamente los valores.</span><span class="sxs-lookup"><span data-stu-id="b4075-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4075-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4075-117">Requirements</span></span>



| <span data-ttu-id="b4075-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4075-118">Requirement</span></span> | <span data-ttu-id="b4075-119">Value</span><span class="sxs-lookup"><span data-stu-id="b4075-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4075-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4075-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4075-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4075-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b4075-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4075-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4075-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4075-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4075-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4075-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4075-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b4075-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4075-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4075-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4075-127">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="b4075-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="b4075-128">**SystemMonitor.ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="b4075-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





