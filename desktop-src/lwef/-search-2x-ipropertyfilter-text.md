---
title: Propiedad de texto IPropertyFilter (WdsSharedIDL. h)
description: Texto del filtro.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Propiedades de texto características de entorno de Windows heredadas
- Propiedades de texto heredadas características de entorno de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534701"
---
# <a name="ipropertyfiltertext-property"></a><span data-ttu-id="cb1b7-106">IPropertyFilter:: Text (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cb1b7-106">IPropertyFilter::Text property</span></span>

> [!NOTE]
> <span data-ttu-id="cb1b7-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cb1b7-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cb1b7-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cb1b7-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="cb1b7-109">Texto del filtro.</span><span class="sxs-lookup"><span data-stu-id="cb1b7-109">Text of the filter.</span></span>

<span data-ttu-id="cb1b7-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cb1b7-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1b7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb1b7-111">Syntax</span></span>


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="cb1b7-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cb1b7-112">Property value</span></span>

<span data-ttu-id="cb1b7-113">Establece el texto del filtro.</span><span class="sxs-lookup"><span data-stu-id="cb1b7-113">Sets the filter text.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb1b7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb1b7-114">Requirements</span></span>



| <span data-ttu-id="cb1b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb1b7-115">Requirement</span></span> | <span data-ttu-id="cb1b7-116">Value</span><span class="sxs-lookup"><span data-stu-id="cb1b7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1b7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb1b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb1b7-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb1b7-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cb1b7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb1b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb1b7-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="cb1b7-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb1b7-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="cb1b7-121">Redistributable</span></span><br/>          | <span data-ttu-id="cb1b7-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="cb1b7-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="cb1b7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb1b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb1b7-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb1b7-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





