---
title: Propiedad IResultsViewer DisplayName (WdsView. h)
description: Nombre para mostrar localizado del tipo.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695914"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="de444-106">IResultsViewer::D propiedad isplayName</span><span class="sxs-lookup"><span data-stu-id="de444-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="de444-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="de444-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="de444-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="de444-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="de444-109">Nombre para mostrar localizado del tipo.</span><span class="sxs-lookup"><span data-stu-id="de444-109">Localized display name of the type.</span></span>

<span data-ttu-id="de444-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de444-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de444-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de444-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="de444-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de444-112">Property value</span></span>

<span data-ttu-id="de444-113">Puntero a un valor que recibe el nombre para mostrar adaptado para el tipo.</span><span class="sxs-lookup"><span data-stu-id="de444-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="de444-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de444-114">Requirements</span></span>



| <span data-ttu-id="de444-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="de444-115">Requirement</span></span> | <span data-ttu-id="de444-116">Value</span><span class="sxs-lookup"><span data-stu-id="de444-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de444-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de444-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de444-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="de444-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de444-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de444-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de444-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="de444-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="de444-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="de444-121">Redistributable</span></span><br/>          | <span data-ttu-id="de444-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="de444-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="de444-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de444-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="de444-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="de444-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





