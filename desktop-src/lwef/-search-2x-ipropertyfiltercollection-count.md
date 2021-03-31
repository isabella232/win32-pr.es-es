---
title: Propiedad de recuento de IPropertyFilterCollection (WdsSharedIDL. h)
description: Número de filtros de la colección.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Propiedad Count características de entorno de Windows heredadas
- Propiedad Count características de entorno heredado de Windows, interfaz IPropertyFilterCollection
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, propiedad Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801934"
---
# <a name="ipropertyfiltercollectioncount-property"></a><span data-ttu-id="0564f-106">IPropertyFilterCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0564f-106">IPropertyFilterCollection::Count property</span></span>

> [!NOTE]
> <span data-ttu-id="0564f-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0564f-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0564f-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0564f-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0564f-109">Número de filtros de la colección.</span><span class="sxs-lookup"><span data-stu-id="0564f-109">Number of filters in the collection.</span></span>

<span data-ttu-id="0564f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0564f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0564f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0564f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="0564f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0564f-112">Property value</span></span>

<span data-ttu-id="0564f-113">Devuelve un puntero al número de filtros de la colección.</span><span class="sxs-lookup"><span data-stu-id="0564f-113">returns a pointer to the number of filters in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0564f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0564f-114">Requirements</span></span>



| <span data-ttu-id="0564f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0564f-115">Requirement</span></span> | <span data-ttu-id="0564f-116">Value</span><span class="sxs-lookup"><span data-stu-id="0564f-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0564f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0564f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0564f-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0564f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0564f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0564f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0564f-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="0564f-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0564f-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0564f-121">Redistributable</span></span><br/>          | <span data-ttu-id="0564f-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="0564f-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="0564f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0564f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0564f-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0564f-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





