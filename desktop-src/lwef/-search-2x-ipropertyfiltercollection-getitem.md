---
title: Propiedad GetITem de IPropertyFilterCollection (WdsSharedIDL. h)
description: Devuelve un filtro específico dentro de la colección.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Propiedad GetITem características de entorno de Windows heredado
- Propiedad GetITem características de entorno heredado de Windows, interfaz IPropertyFilterCollection
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, propiedad GetITem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996241"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a><span data-ttu-id="50982-106">IPropertyFilterCollection:: GetITem (propiedad)</span><span class="sxs-lookup"><span data-stu-id="50982-106">IPropertyFilterCollection::GetITem property</span></span>

> [!NOTE]
> <span data-ttu-id="50982-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="50982-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="50982-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="50982-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="50982-109">Devuelve un filtro específico dentro de la colección.</span><span class="sxs-lookup"><span data-stu-id="50982-109">Returns a specific filter within the collection.</span></span>

<span data-ttu-id="50982-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="50982-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="50982-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50982-111">Syntax</span></span>


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="50982-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="50982-112">Property value</span></span>

<span data-ttu-id="50982-113">Establece la dirección del filtro.</span><span class="sxs-lookup"><span data-stu-id="50982-113">Sets the address of the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="50982-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50982-114">Requirements</span></span>



| <span data-ttu-id="50982-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="50982-115">Requirement</span></span> | <span data-ttu-id="50982-116">Value</span><span class="sxs-lookup"><span data-stu-id="50982-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="50982-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50982-117">Minimum supported client</span></span><br/> | <span data-ttu-id="50982-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="50982-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="50982-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50982-119">Minimum supported server</span></span><br/> | <span data-ttu-id="50982-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="50982-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="50982-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="50982-121">Redistributable</span></span><br/>          | <span data-ttu-id="50982-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="50982-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="50982-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50982-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50982-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="50982-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





