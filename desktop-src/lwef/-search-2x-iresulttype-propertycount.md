---
title: Propiedad IResultType PropertyCount (WdsSharedIDL. h)
description: Esta propiedad contiene el número de propiedades expuestas por el tipo.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Propiedad PropertyCount características de entorno heredado de Windows
- Propiedad PropertyCount características de entorno heredado de Windows, interfaz IResultType
- Interfaz IResultType características del entorno heredado de Windows, propiedad PropertyCount
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533777"
---
# <a name="iresulttypepropertycount-property"></a><span data-ttu-id="e1bf4-106">IResultType::P propiedad ropertyCount</span><span class="sxs-lookup"><span data-stu-id="e1bf4-106">IResultType::PropertyCount property</span></span>

> [!NOTE]
> <span data-ttu-id="e1bf4-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e1bf4-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e1bf4-109">Esta propiedad contiene el número de propiedades expuestas por el tipo.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-109">This property contains the number of properties exposed by the type.</span></span>

<span data-ttu-id="e1bf4-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bf4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1bf4-111">Syntax</span></span>


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="e1bf4-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e1bf4-112">Property value</span></span>

<span data-ttu-id="e1bf4-113">Devuelve la dirección del número de propiedades expuestas.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-113">returns the address of the number of properties exposed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1bf4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1bf4-114">Requirements</span></span>



| <span data-ttu-id="e1bf4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1bf4-115">Requirement</span></span> | <span data-ttu-id="e1bf4-116">Value</span><span class="sxs-lookup"><span data-stu-id="e1bf4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bf4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1bf4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1bf4-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1bf4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e1bf4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1bf4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1bf4-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="e1bf4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1bf4-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e1bf4-121">Redistributable</span></span><br/>          | <span data-ttu-id="e1bf4-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e1bf4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="e1bf4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1bf4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1bf4-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1bf4-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





