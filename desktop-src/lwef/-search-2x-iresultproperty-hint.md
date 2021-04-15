---
title: Propiedad de sugerencia IResultProperty (WdsSharedIDL. h)
description: Valor especial que se usa para ayudar a la recuperación de datos.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Propiedad Hint características heredadas del entorno de Windows
- Propiedad Hint características de entorno de Windows heredadas, interfaz IResultProperty
- Interfaz IResultProperty características de entorno heredado de Windows, propiedad Hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695892"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="634f6-106">IResultProperty:: Hint (propiedad)</span><span class="sxs-lookup"><span data-stu-id="634f6-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="634f6-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="634f6-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="634f6-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="634f6-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="634f6-109">Valor especial que se usa para ayudar a la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="634f6-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="634f6-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="634f6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="634f6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="634f6-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="634f6-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="634f6-112">Property value</span></span>

<span data-ttu-id="634f6-113">Devuelve un puntero a la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="634f6-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="634f6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="634f6-114">Requirements</span></span>



| <span data-ttu-id="634f6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="634f6-115">Requirement</span></span> | <span data-ttu-id="634f6-116">Value</span><span class="sxs-lookup"><span data-stu-id="634f6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="634f6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="634f6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="634f6-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="634f6-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="634f6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="634f6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="634f6-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="634f6-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="634f6-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="634f6-121">Redistributable</span></span><br/>          | <span data-ttu-id="634f6-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="634f6-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="634f6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="634f6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="634f6-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="634f6-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





