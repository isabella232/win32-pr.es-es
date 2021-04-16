---
title: Propiedad IResultsViewer SortOrderProperty (WdsView.h)
description: Esta propiedad establece o devuelve el orden de las columnas por las que se van a ordenar los resultados.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Propiedad SortOrderProperty características de entorno heredado de Windows
- Propiedad SortOrderProperty características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad SortOrderProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676743"
---
# <a name="iresultsviewersortorderproperty-property"></a><span data-ttu-id="ad618-106">IResultsViewer:: SortOrderProperty (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ad618-106">IResultsViewer::SortOrderProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="ad618-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ad618-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ad618-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ad618-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="ad618-109">Esta propiedad establece o devuelve el orden de las columnas por las que se van a ordenar los resultados.</span><span class="sxs-lookup"><span data-stu-id="ad618-109">This property will set or return the order of columns to sort results by.</span></span>

<span data-ttu-id="ad618-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ad618-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad618-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad618-111">Syntax</span></span>


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a><span data-ttu-id="ad618-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ad618-112">Property value</span></span>

<span data-ttu-id="ad618-113">Establece la propiedad [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .</span><span class="sxs-lookup"><span data-stu-id="ad618-113">Sets the [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad618-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad618-114">Requirements</span></span>



| <span data-ttu-id="ad618-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad618-115">Requirement</span></span> | <span data-ttu-id="ad618-116">Value</span><span class="sxs-lookup"><span data-stu-id="ad618-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad618-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad618-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad618-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad618-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ad618-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad618-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad618-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="ad618-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="ad618-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ad618-121">Redistributable</span></span><br/>          | <span data-ttu-id="ad618-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="ad618-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="ad618-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad618-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad618-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad618-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





