---
title: Propiedad IResultVerb HelpText (WdsSharedIDL. h)
description: Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- HelpText propiedad características de entorno heredado de Windows
- HelpText propiedad características de entorno heredado de Windows, interfaz IResultVerb
- Interfaz IResultVerb características del entorno heredado de Windows, HelpText (propiedad)
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801927"
---
# <a name="iresultverbhelptext-property"></a><span data-ttu-id="13309-106">IResultVerb:: HelpText (propiedad)</span><span class="sxs-lookup"><span data-stu-id="13309-106">IResultVerb::HelpText property</span></span>

> [!NOTE]
> <span data-ttu-id="13309-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="13309-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="13309-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="13309-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="13309-109">Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo.</span><span class="sxs-lookup"><span data-stu-id="13309-109">This property returns a pointer to the localized help string for the verb.</span></span>

<span data-ttu-id="13309-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="13309-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13309-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13309-111">Syntax</span></span>


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="13309-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="13309-112">Property value</span></span>

<span data-ttu-id="13309-113">El valor de esta propiedad es un puntero a la cadena de ayuda localizada para este verbo.</span><span class="sxs-lookup"><span data-stu-id="13309-113">The value of this property is a pointer to the localized help string for this verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="13309-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13309-114">Requirements</span></span>



| <span data-ttu-id="13309-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="13309-115">Requirement</span></span> | <span data-ttu-id="13309-116">Value</span><span class="sxs-lookup"><span data-stu-id="13309-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="13309-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13309-117">Minimum supported client</span></span><br/> | <span data-ttu-id="13309-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="13309-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="13309-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13309-119">Minimum supported server</span></span><br/> | <span data-ttu-id="13309-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="13309-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13309-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="13309-121">Redistributable</span></span><br/>          | <span data-ttu-id="13309-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="13309-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="13309-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13309-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="13309-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="13309-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





