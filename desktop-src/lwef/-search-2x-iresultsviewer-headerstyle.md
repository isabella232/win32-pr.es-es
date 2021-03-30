---
title: Propiedad HeaderStyle de IResultsViewer (WdsView. h)
description: Estilo del encabezado que se muestra en la vista.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Propiedad HeaderStyle características de entorno de Windows heredadas
- HeaderStyle (propiedad) características del entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad HeaderStyle
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802347"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="6f6d2-106">IResultsViewer:: HeaderStyle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6f6d2-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="6f6d2-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6f6d2-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6f6d2-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="6f6d2-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6f6d2-109">Estilo del encabezado que se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="6f6d2-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="6f6d2-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6f6d2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6d2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f6d2-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="6f6d2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6f6d2-112">Property value</span></span>

<span data-ttu-id="6f6d2-113">Establece el estilo del encabezado que se muestra.</span><span class="sxs-lookup"><span data-stu-id="6f6d2-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f6d2-114">Requirements</span></span>



| <span data-ttu-id="6f6d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f6d2-115">Requirement</span></span> | <span data-ttu-id="6f6d2-116">Value</span><span class="sxs-lookup"><span data-stu-id="6f6d2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6d2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f6d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6d2-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f6d2-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6f6d2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f6d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6d2-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="6f6d2-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="6f6d2-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6f6d2-121">Redistributable</span></span><br/>          | <span data-ttu-id="6f6d2-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6f6d2-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="6f6d2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f6d2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f6d2-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f6d2-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





