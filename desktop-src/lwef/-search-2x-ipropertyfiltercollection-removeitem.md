---
title: Propiedad RemoveItem de IPropertyFilterCollection (WdsSharedIDL. h)
description: Quita un filtro específico de la colección.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Propiedades de RemoveItem características de entorno de Windows heredadas
- Propiedades de RemoveItem características de entorno de Windows heredadas, interfaz IPropertyFilterCollection
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, propiedad RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802894"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a><span data-ttu-id="3c2d8-106">IPropertyFilterCollection:: RemoveItem (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3c2d8-106">IPropertyFilterCollection::RemoveItem property</span></span>

> [!NOTE]
> <span data-ttu-id="3c2d8-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3c2d8-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3c2d8-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3c2d8-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="3c2d8-109">Quita un filtro específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="3c2d8-109">Removes a specific filter to the collection.</span></span>

<span data-ttu-id="3c2d8-110">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="3c2d8-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2d8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c2d8-111">Syntax</span></span>


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a><span data-ttu-id="3c2d8-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c2d8-112">Property value</span></span>

<span data-ttu-id="3c2d8-113">Acepta un puntero al índice del filtro que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="3c2d8-113">Accepts a pointer to the index for the filter to be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2d8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c2d8-114">Requirements</span></span>



| <span data-ttu-id="3c2d8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c2d8-115">Requirement</span></span> | <span data-ttu-id="3c2d8-116">Value</span><span class="sxs-lookup"><span data-stu-id="3c2d8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2d8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c2d8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2d8-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c2d8-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3c2d8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c2d8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2d8-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="3c2d8-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c2d8-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3c2d8-121">Redistributable</span></span><br/>          | <span data-ttu-id="3c2d8-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="3c2d8-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="3c2d8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c2d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2d8-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2d8-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





