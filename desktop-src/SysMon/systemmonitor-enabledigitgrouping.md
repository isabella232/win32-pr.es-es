---
title: Propiedad SystemMonitor. EnableDigitGrouping
description: Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propiedad EnableDigitGrouping SysMon
- Propiedad EnableDigitGrouping SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422342"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="fac95-106">Propiedad SystemMonitor. EnableDigitGrouping</span><span class="sxs-lookup"><span data-stu-id="fac95-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="fac95-107">Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="fac95-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac95-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fac95-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="fac95-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fac95-109">Property value</span></span>

<span data-ttu-id="fac95-110">Si es true, SYSMON agrupará los dígitos al mostrar valores numéricos, por ejemplo, 1.214.</span><span class="sxs-lookup"><span data-stu-id="fac95-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="fac95-111">Si es false, los valores numéricos no se agrupan, por ejemplo, 1214.</span><span class="sxs-lookup"><span data-stu-id="fac95-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="fac95-112">True es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fac95-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac95-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fac95-113">Remarks</span></span>

<span data-ttu-id="fac95-114">Se localiza el símbolo de agrupación de dígitos.</span><span class="sxs-lookup"><span data-stu-id="fac95-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac95-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac95-115">Requirements</span></span>



| <span data-ttu-id="fac95-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac95-116">Requirement</span></span> | <span data-ttu-id="fac95-117">Value</span><span class="sxs-lookup"><span data-stu-id="fac95-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fac95-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fac95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fac95-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fac95-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fac95-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fac95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fac95-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fac95-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fac95-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fac95-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac95-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="fac95-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





