---
title: Propiedad IResultsViewer PreviewStyle (WdsView. h)
description: Controla el modo de presentación del panel de vista previa.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Propiedad PreviewStyle características de entorno heredado de Windows
- Propiedad PreviewStyle características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad PreviewStyle
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714541"
---
# <a name="iresultsviewerpreviewstyle-property"></a><span data-ttu-id="70f97-106">IResultsViewer::P propiedad reviewStyle</span><span class="sxs-lookup"><span data-stu-id="70f97-106">IResultsViewer::PreviewStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="70f97-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70f97-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="70f97-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="70f97-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="70f97-109">Controla el modo de presentación del panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="70f97-109">Controls the preview pane's display mode.</span></span>

<span data-ttu-id="70f97-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="70f97-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f97-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70f97-111">Syntax</span></span>


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="70f97-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="70f97-112">Property value</span></span>

<span data-ttu-id="70f97-113">Establece la propiedad de estilo actual para el panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="70f97-113">Sets the current style property for the preview pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="70f97-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70f97-114">Requirements</span></span>



| <span data-ttu-id="70f97-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f97-115">Requirement</span></span> | <span data-ttu-id="70f97-116">Value</span><span class="sxs-lookup"><span data-stu-id="70f97-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="70f97-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70f97-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70f97-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="70f97-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="70f97-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70f97-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70f97-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="70f97-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="70f97-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="70f97-121">Redistributable</span></span><br/>          | <span data-ttu-id="70f97-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="70f97-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="70f97-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70f97-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="70f97-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="70f97-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





