---
title: Propiedad UID de IResultProperty (WdsSharedIDL. h)
description: Identificador único de la propiedad.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Propiedad UID características de entorno heredado de Windows
- Propiedad UID características de entorno heredado de Windows, interfaz IResultProperty
- Interfaz IResultProperty características del entorno heredado de Windows, propiedad UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079227"
---
# <a name="iresultpropertyuid-property"></a><span data-ttu-id="b69b9-106">IResultProperty:: UID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b69b9-106">IResultProperty::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="b69b9-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b69b9-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b69b9-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b69b9-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b69b9-109">Identificador único de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b69b9-109">Unique identifier for the property.</span></span>

<span data-ttu-id="b69b9-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b69b9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b69b9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b69b9-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="b69b9-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b69b9-112">Property value</span></span>

<span data-ttu-id="b69b9-113">Devuelve un puntero al identificador único de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b69b9-113">returns a pointer to the unique property identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="b69b9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b69b9-114">Requirements</span></span>



| <span data-ttu-id="b69b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b69b9-115">Requirement</span></span> | <span data-ttu-id="b69b9-116">Value</span><span class="sxs-lookup"><span data-stu-id="b69b9-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b69b9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b69b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b69b9-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b69b9-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b69b9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b69b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b69b9-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="b69b9-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b69b9-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b69b9-121">Redistributable</span></span><br/>          | <span data-ttu-id="b69b9-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="b69b9-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="b69b9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b69b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b69b9-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b69b9-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





