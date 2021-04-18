---
title: Propiedad IPropertyFilter LogicOperator (WdsSharedIDL. h)
description: Operador lógico que se va a usar al aplicar un filtro.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Propiedad LogicOperator características de entorno heredado de Windows
- Propiedad LogicOperator características de entorno heredado de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493066"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="d3f4b-106">IPropertyFilter:: LogicOperator (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d3f4b-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="d3f4b-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d3f4b-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d3f4b-109">Operador lógico que se va a usar al aplicar un filtro.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="d3f4b-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f4b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3f4b-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="d3f4b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d3f4b-112">Property value</span></span>

<span data-ttu-id="d3f4b-113">Establece el tipo de operador lógico.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f4b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f4b-114">Requirements</span></span>



| <span data-ttu-id="d3f4b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f4b-115">Requirement</span></span> | <span data-ttu-id="d3f4b-116">Value</span><span class="sxs-lookup"><span data-stu-id="d3f4b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f4b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3f4b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f4b-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3f4b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d3f4b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3f4b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f4b-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="d3f4b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3f4b-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d3f4b-121">Redistributable</span></span><br/>          | <span data-ttu-id="d3f4b-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d3f4b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d3f4b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3f4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f4b-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f4b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





