---
title: Propiedad FilterType de IResultsViewer (WdsView. h)
description: Esta propiedad establece o devuelve el nombre del tipo preceived por el que se van a filtrar los resultados.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- Propiedad FilterType características de entorno de Windows heredadas
- Propiedad FilterType características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad FilterType
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696050"
---
# <a name="iresultsviewerfiltertype-property"></a><span data-ttu-id="b1747-106">IResultsViewer:: FilterType (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b1747-106">IResultsViewer::FilterType property</span></span>

> [!NOTE]
> <span data-ttu-id="b1747-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1747-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b1747-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b1747-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b1747-109">Esta propiedad establece o devuelve el nombre del tipo preceived por el que se van a filtrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="b1747-109">This property will set or return the name of the preceived type to filter results by.</span></span>

<span data-ttu-id="b1747-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b1747-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1747-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1747-111">Syntax</span></span>


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="b1747-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b1747-112">Property value</span></span>

<span data-ttu-id="b1747-113">Establece el tipo percibido que se usa para filtrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="b1747-113">Sets the perceived type used to filter results.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1747-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1747-114">Requirements</span></span>



| <span data-ttu-id="b1747-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1747-115">Requirement</span></span> | <span data-ttu-id="b1747-116">Value</span><span class="sxs-lookup"><span data-stu-id="b1747-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1747-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1747-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1747-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1747-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1747-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1747-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1747-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="b1747-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b1747-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b1747-121">Redistributable</span></span><br/>          | <span data-ttu-id="b1747-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="b1747-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="b1747-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1747-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1747-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1747-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





