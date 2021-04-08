---
title: Propiedad de peritem. Selected
description: Recupera o establece un valor que indica si el contador está seleccionado.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propiedad seleccionada SysMon
- Propiedad seleccionada SysMon, objeto de contraelemento
- Objeto de perelemento SysMon, propiedad seleccionada
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996495"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="8d09b-106">Propiedad de peritem. Selected</span><span class="sxs-lookup"><span data-stu-id="8d09b-106">CounterItem.Selected property</span></span>

<span data-ttu-id="8d09b-107">Recupera o establece un valor que indica si el contador está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8d09b-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="8d09b-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8d09b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d09b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d09b-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8d09b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8d09b-110">Property value</span></span>

<span data-ttu-id="8d09b-111">True si el contador está seleccionado; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="8d09b-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d09b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d09b-112">Remarks</span></span>

<span data-ttu-id="8d09b-113">Puede seleccionar uno o varios contadores de la colección de contadores.</span><span class="sxs-lookup"><span data-stu-id="8d09b-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="8d09b-114">Seleccionar un contador, selecciona el contador en la leyenda, hace que el contador esté visible en la leyenda y genera un evento [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .</span><span class="sxs-lookup"><span data-stu-id="8d09b-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d09b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d09b-115">Requirements</span></span>



| <span data-ttu-id="8d09b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d09b-116">Requirement</span></span> | <span data-ttu-id="8d09b-117">Value</span><span class="sxs-lookup"><span data-stu-id="8d09b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d09b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d09b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8d09b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d09b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d09b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d09b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8d09b-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d09b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d09b-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d09b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d09b-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8d09b-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d09b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d09b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d09b-125">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="8d09b-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





