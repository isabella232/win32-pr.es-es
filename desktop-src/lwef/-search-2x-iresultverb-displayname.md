---
title: Propiedad IResultVerb DisplayName (WdsSharedIDL. h)
description: Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultVerb
- Interfaz IResultVerb características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079225"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="06ba4-106">IResultVerb::D propiedad isplayName</span><span class="sxs-lookup"><span data-stu-id="06ba4-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="06ba4-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="06ba4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="06ba4-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="06ba4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="06ba4-109">Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.</span><span class="sxs-lookup"><span data-stu-id="06ba4-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="06ba4-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="06ba4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ba4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06ba4-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="06ba4-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="06ba4-112">Property value</span></span>

<span data-ttu-id="06ba4-113">Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.</span><span class="sxs-lookup"><span data-stu-id="06ba4-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ba4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06ba4-114">Requirements</span></span>



| <span data-ttu-id="06ba4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="06ba4-115">Requirement</span></span> | <span data-ttu-id="06ba4-116">Value</span><span class="sxs-lookup"><span data-stu-id="06ba4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ba4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06ba4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06ba4-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="06ba4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="06ba4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06ba4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06ba4-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="06ba4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06ba4-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="06ba4-121">Redistributable</span></span><br/>          | <span data-ttu-id="06ba4-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="06ba4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="06ba4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06ba4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06ba4-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="06ba4-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





