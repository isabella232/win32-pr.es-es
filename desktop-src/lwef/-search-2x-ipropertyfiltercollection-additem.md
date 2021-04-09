---
title: Propiedad IPropertyFilterCollection AddItem (WdsSharedIDL. h)
description: Agrega un nuevo filtro a la colección.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Propiedad AddItem características de entorno de Windows heredadas
- Propiedad AddItem características de entorno de Windows heredadas, interfaz IPropertyFilterCollection
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, propiedad AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079228"
---
# <a name="ipropertyfiltercollectionadditem-property"></a><span data-ttu-id="709f7-106">IPropertyFilterCollection:: AddItem (propiedad)</span><span class="sxs-lookup"><span data-stu-id="709f7-106">IPropertyFilterCollection::AddItem property</span></span>

> [!NOTE]
> <span data-ttu-id="709f7-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="709f7-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="709f7-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="709f7-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="709f7-109">Agrega un nuevo filtro a la colección.</span><span class="sxs-lookup"><span data-stu-id="709f7-109">Adds a new filter to the collection.</span></span>

<span data-ttu-id="709f7-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="709f7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="709f7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="709f7-111">Syntax</span></span>


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="709f7-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="709f7-112">Property value</span></span>

<span data-ttu-id="709f7-113">Devuelve un puntero a la dirección para el nuevo filtro.</span><span class="sxs-lookup"><span data-stu-id="709f7-113">returns a pointer to the address for the new filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="709f7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="709f7-114">Requirements</span></span>



| <span data-ttu-id="709f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="709f7-115">Requirement</span></span> | <span data-ttu-id="709f7-116">Value</span><span class="sxs-lookup"><span data-stu-id="709f7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="709f7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="709f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="709f7-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="709f7-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="709f7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="709f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="709f7-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="709f7-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="709f7-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="709f7-121">Redistributable</span></span><br/>          | <span data-ttu-id="709f7-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="709f7-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="709f7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="709f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="709f7-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="709f7-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





