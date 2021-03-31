---
title: Propiedad de icono IResultVerb (WdsSharedIDL. h)
description: Esta propiedad devuelve un puntero al identificador del icono opcional asociado al verbo.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Propiedad de icono características de entorno de Windows heredadas
- Propiedad de icono características de entorno heredado de Windows, interfaz IResultVerb
- Interfaz IResultVerb características del entorno heredado de Windows, propiedad Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491560"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="48a31-106">IResultVerb:: Icon (propiedad)</span><span class="sxs-lookup"><span data-stu-id="48a31-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="48a31-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="48a31-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="48a31-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="48a31-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="48a31-109">Esta propiedad devuelve un puntero al identificador del icono opcional asociado al verbo.</span><span class="sxs-lookup"><span data-stu-id="48a31-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="48a31-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48a31-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a31-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48a31-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="48a31-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="48a31-112">Property value</span></span>

<span data-ttu-id="48a31-113">HICON es un puntero al identificador del icono opcional assocuated con el verbo.</span><span class="sxs-lookup"><span data-stu-id="48a31-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a31-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a31-114">Requirements</span></span>



| <span data-ttu-id="48a31-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a31-115">Requirement</span></span> | <span data-ttu-id="48a31-116">Value</span><span class="sxs-lookup"><span data-stu-id="48a31-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a31-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a31-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48a31-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="48a31-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="48a31-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a31-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48a31-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="48a31-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48a31-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="48a31-121">Redistributable</span></span><br/>          | <span data-ttu-id="48a31-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="48a31-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="48a31-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48a31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a31-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a31-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





