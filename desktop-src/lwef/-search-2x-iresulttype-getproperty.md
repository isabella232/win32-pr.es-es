---
title: Propiedad IResultType GetProperty (WdsSharedIDL. h)
description: Esta propiedad contiene información de propiedad especificada.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Propiedad GetProperty características de entorno heredado de Windows
- Propiedad GetProperty características de entorno heredado de Windows, interfaz IResultType
- Interfaz IResultType características del entorno heredado de Windows, propiedad GetProperty
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905145"
---
# <a name="iresulttypegetproperty-property"></a><span data-ttu-id="2299c-106">IResultType:: GetProperty (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2299c-106">IResultType::GetProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="2299c-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2299c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2299c-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2299c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2299c-109">Esta propiedad contiene información de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="2299c-109">This property contains specified property information.</span></span>

<span data-ttu-id="2299c-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2299c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2299c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2299c-111">Syntax</span></span>


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a><span data-ttu-id="2299c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2299c-112">Property value</span></span>

<span data-ttu-id="2299c-113">Establece la dirección de la información de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="2299c-113">Sets the address of the specified property information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2299c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2299c-114">Requirements</span></span>



| <span data-ttu-id="2299c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2299c-115">Requirement</span></span> | <span data-ttu-id="2299c-116">Value</span><span class="sxs-lookup"><span data-stu-id="2299c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2299c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2299c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2299c-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2299c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2299c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2299c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2299c-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="2299c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2299c-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2299c-121">Redistributable</span></span><br/>          | <span data-ttu-id="2299c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="2299c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="2299c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2299c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2299c-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2299c-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





