---
title: Propiedad IResultProperty DisplayState (WdsSharedIDL. h)
description: Visability de la propiedad.
ms.assetid: 4fdf6cdb-30bd-4582-a573-a1cc9f4052e6
keywords:
- Propiedad DisplayState características de entorno heredado de Windows
- Propiedad DisplayState características de entorno heredado de Windows, interfaz IResultProperty
- Interfaz IResultProperty características del entorno heredado de Windows, propiedad DisplayState
topic_type:
- apiref
api_name:
- IResultProperty.DisplayState
- IResultProperty.get_DisplayState
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85634441a38c2cb2130010c79f8ee3ebcb78a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695969"
---
# <a name="iresultpropertydisplaystate-property"></a><span data-ttu-id="e241e-106">IResultProperty::D propiedad isplayState</span><span class="sxs-lookup"><span data-stu-id="e241e-106">IResultProperty::DisplayState property</span></span>

> [!NOTE]
> <span data-ttu-id="e241e-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e241e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e241e-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e241e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e241e-109">Visability de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e241e-109">Visability of the property.</span></span>

<span data-ttu-id="e241e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e241e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e241e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e241e-111">Syntax</span></span>


```C++
HRESULT get_DisplayState(
  [out, retval] PropertyDisplayState *state
);
```



## <a name="property-value"></a><span data-ttu-id="e241e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e241e-112">Property value</span></span>

<span data-ttu-id="e241e-113">Devuelve un puntero al valor del estado de presentación.</span><span class="sxs-lookup"><span data-stu-id="e241e-113">returns a pointer to the display state value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e241e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e241e-114">Requirements</span></span>



| <span data-ttu-id="e241e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e241e-115">Requirement</span></span> | <span data-ttu-id="e241e-116">Value</span><span class="sxs-lookup"><span data-stu-id="e241e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e241e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e241e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e241e-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e241e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e241e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e241e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e241e-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="e241e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e241e-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e241e-121">Redistributable</span></span><br/>          | <span data-ttu-id="e241e-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e241e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="e241e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e241e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e241e-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e241e-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





