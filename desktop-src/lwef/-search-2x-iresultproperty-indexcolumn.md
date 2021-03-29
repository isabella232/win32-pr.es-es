---
title: Propiedad IResultProperty IndexColumn (WdsSharedIDL. h)
description: Nombre de la columna de propiedades en el índice.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Propiedad IndexColumn características de entorno heredado de Windows
- Propiedad IndexColumn características de entorno heredado de Windows, interfaz IResultProperty
- Interfaz IResultProperty características del entorno heredado de Windows, propiedad IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905146"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="abbdc-106">IResultProperty:: IndexColumn (propiedad)</span><span class="sxs-lookup"><span data-stu-id="abbdc-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="abbdc-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="abbdc-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="abbdc-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="abbdc-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="abbdc-109">Nombre de la columna de propiedades en el índice.</span><span class="sxs-lookup"><span data-stu-id="abbdc-109">Properties column name in the index.</span></span>

<span data-ttu-id="abbdc-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="abbdc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="abbdc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abbdc-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="abbdc-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="abbdc-112">Property value</span></span>

<span data-ttu-id="abbdc-113">Devuelve un puntero al nombre de la columna en el índice.</span><span class="sxs-lookup"><span data-stu-id="abbdc-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="abbdc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abbdc-114">Requirements</span></span>



| <span data-ttu-id="abbdc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="abbdc-115">Requirement</span></span> | <span data-ttu-id="abbdc-116">Value</span><span class="sxs-lookup"><span data-stu-id="abbdc-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="abbdc-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abbdc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="abbdc-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="abbdc-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="abbdc-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abbdc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="abbdc-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="abbdc-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="abbdc-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="abbdc-121">Redistributable</span></span><br/>          | <span data-ttu-id="abbdc-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="abbdc-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="abbdc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abbdc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="abbdc-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="abbdc-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





