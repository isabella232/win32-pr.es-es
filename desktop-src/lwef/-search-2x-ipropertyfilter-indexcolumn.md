---
title: Propiedad IPropertyFilter IndexColumn (WdsSharedIDL. h)
description: Nombre de columna indizada de la propiedad por la que se va a filtrar.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Propiedad IndexColumn características de entorno heredado de Windows
- Propiedad IndexColumn características de entorno heredado de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad IndexColumn
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079322"
---
# <a name="ipropertyfilterindexcolumn-property"></a><span data-ttu-id="134c8-106">IPropertyFilter:: IndexColumn (propiedad)</span><span class="sxs-lookup"><span data-stu-id="134c8-106">IPropertyFilter::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="134c8-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="134c8-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="134c8-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="134c8-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="134c8-109">Nombre de columna indizada de la propiedad por la que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="134c8-109">Indexed column name of the property to filter by.</span></span>

<span data-ttu-id="134c8-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="134c8-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="134c8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="134c8-111">Syntax</span></span>


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="134c8-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="134c8-112">Property value</span></span>

<span data-ttu-id="134c8-113">Establece la propiedad de columna.</span><span class="sxs-lookup"><span data-stu-id="134c8-113">Sets the Column property.</span></span>

## <a name="requirements"></a><span data-ttu-id="134c8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="134c8-114">Requirements</span></span>



| <span data-ttu-id="134c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="134c8-115">Requirement</span></span> | <span data-ttu-id="134c8-116">Value</span><span class="sxs-lookup"><span data-stu-id="134c8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="134c8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="134c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="134c8-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="134c8-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="134c8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="134c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="134c8-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="134c8-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="134c8-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="134c8-121">Redistributable</span></span><br/>          | <span data-ttu-id="134c8-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="134c8-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="134c8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="134c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="134c8-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="134c8-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





