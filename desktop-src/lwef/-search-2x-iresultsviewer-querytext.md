---
title: Propiedad IResultsViewer QueryText (WdsView. h)
description: Obtiene o establece el texto de la consulta actual.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Propiedades de QueryText características de entorno heredado de Windows
- Propiedad QueryText características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150986"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="95510-106">IResultsViewer:: QueryText (propiedad)</span><span class="sxs-lookup"><span data-stu-id="95510-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="95510-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="95510-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="95510-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="95510-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="95510-109">Obtiene o establece el texto de la consulta actual.</span><span class="sxs-lookup"><span data-stu-id="95510-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="95510-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="95510-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="95510-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95510-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="95510-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="95510-112">Property value</span></span>

<span data-ttu-id="95510-113">Establece el texto de la consulta actual.</span><span class="sxs-lookup"><span data-stu-id="95510-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="95510-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95510-114">Requirements</span></span>



| <span data-ttu-id="95510-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="95510-115">Requirement</span></span> | <span data-ttu-id="95510-116">Value</span><span class="sxs-lookup"><span data-stu-id="95510-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95510-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95510-117">Minimum supported client</span></span><br/> | <span data-ttu-id="95510-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="95510-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95510-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95510-119">Minimum supported server</span></span><br/> | <span data-ttu-id="95510-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="95510-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="95510-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="95510-121">Redistributable</span></span><br/>          | <span data-ttu-id="95510-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="95510-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="95510-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95510-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95510-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="95510-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





