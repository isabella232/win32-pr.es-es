---
title: Propiedad IPropertyFilter NestingDepth (WdsSharedIDL. h)
description: Filtra la profundidad dentro de un conjunto anidado de paréntesis.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Propiedad NestingDepth características de entorno heredado de Windows
- Propiedad NestingDepth características de entorno heredado de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422286"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="97266-106">IPropertyFilter:: NestingDepth (propiedad)</span><span class="sxs-lookup"><span data-stu-id="97266-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="97266-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="97266-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="97266-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="97266-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="97266-109">Filtra la profundidad dentro de un conjunto anidado de paréntesis.</span><span class="sxs-lookup"><span data-stu-id="97266-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="97266-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="97266-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="97266-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97266-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="97266-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="97266-112">Property value</span></span>

<span data-ttu-id="97266-113">Establece el número que indica la profundidad de los paréntesis anidados.</span><span class="sxs-lookup"><span data-stu-id="97266-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="97266-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97266-114">Requirements</span></span>



| <span data-ttu-id="97266-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="97266-115">Requirement</span></span> | <span data-ttu-id="97266-116">Value</span><span class="sxs-lookup"><span data-stu-id="97266-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="97266-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97266-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97266-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="97266-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="97266-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97266-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97266-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="97266-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="97266-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="97266-121">Redistributable</span></span><br/>          | <span data-ttu-id="97266-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="97266-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="97266-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97266-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="97266-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="97266-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





