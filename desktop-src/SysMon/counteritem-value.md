---
title: Propiedad de valor de contraitem. Value
description: Recupera el último valor muestreado del contador.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Propiedad de valor SysMon
- Propiedad Value SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad Value
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666014"
---
# <a name="counteritemvalue-property"></a><span data-ttu-id="e39bf-106">Propiedad de valor de contraitem. Value</span><span class="sxs-lookup"><span data-stu-id="e39bf-106">CounterItem.Value property</span></span>

<span data-ttu-id="e39bf-107">Recupera el último valor muestreado del contador.</span><span class="sxs-lookup"><span data-stu-id="e39bf-107">Retrieves the last sampled value of the counter.</span></span>

<span data-ttu-id="e39bf-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e39bf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e39bf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e39bf-109">Syntax</span></span>


```VB
Property Value As Double
```



## <a name="property-value"></a><span data-ttu-id="e39bf-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e39bf-110">Property value</span></span>

<span data-ttu-id="e39bf-111">Último valor muestreado del contador.</span><span class="sxs-lookup"><span data-stu-id="e39bf-111">Last sampled value of the counter.</span></span> <span data-ttu-id="e39bf-112">El valor es-1 si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="e39bf-112">The value is -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="e39bf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e39bf-113">Remarks</span></span>

<span data-ttu-id="e39bf-114">Esta es la propiedad predeterminada del objeto de [**elemento**](counteritem.md) de mismo valor.</span><span class="sxs-lookup"><span data-stu-id="e39bf-114">This is the default property of the [**CounterItem**](counteritem.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e39bf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e39bf-115">Requirements</span></span>



| <span data-ttu-id="e39bf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e39bf-116">Requirement</span></span> | <span data-ttu-id="e39bf-117">Value</span><span class="sxs-lookup"><span data-stu-id="e39bf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e39bf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e39bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e39bf-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e39bf-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e39bf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e39bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e39bf-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e39bf-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e39bf-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e39bf-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e39bf-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e39bf-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e39bf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e39bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39bf-125">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="e39bf-125">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="e39bf-126">**Peritem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="e39bf-126">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





