---
title: Propiedad UID de IPropertyFilter (WdsSharedIDL. h)
description: UID para la propiedad que se va a filtrar.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Propiedad UID características de entorno heredado de Windows
- Propiedad UID características de entorno heredado de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359778"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="f8928-106">IPropertyFilter:: UID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f8928-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="f8928-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f8928-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f8928-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f8928-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f8928-109">UID para la propiedad que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="f8928-109">UID for the property to filter by.</span></span>

<span data-ttu-id="f8928-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f8928-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8928-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8928-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="f8928-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f8928-112">Property value</span></span>

<span data-ttu-id="f8928-113">Establece la propiedad UID.</span><span class="sxs-lookup"><span data-stu-id="f8928-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8928-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8928-114">Requirements</span></span>



| <span data-ttu-id="f8928-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8928-115">Requirement</span></span> | <span data-ttu-id="f8928-116">Value</span><span class="sxs-lookup"><span data-stu-id="f8928-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8928-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8928-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8928-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8928-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f8928-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8928-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8928-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="f8928-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f8928-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f8928-121">Redistributable</span></span><br/>          | <span data-ttu-id="f8928-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="f8928-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="f8928-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8928-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8928-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8928-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





