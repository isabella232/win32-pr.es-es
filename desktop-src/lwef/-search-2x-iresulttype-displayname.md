---
title: Propiedad IResultType DisplayName (WdsSharedIDL. h)
description: Nombre para mostrar localizado del tipo
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultType
- Interfaz IResultType características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94080a2b5c6121bbaa9b611a7d55c2d5aaeed5e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705131"
---
# <a name="iresulttypedisplayname-property"></a><span data-ttu-id="2cb67-106">IResultType::D propiedad isplayName</span><span class="sxs-lookup"><span data-stu-id="2cb67-106">IResultType::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="2cb67-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2cb67-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2cb67-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2cb67-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2cb67-109">Nombre para mostrar localizado del tipo:</span><span class="sxs-lookup"><span data-stu-id="2cb67-109">Localized display name of the type:</span></span>

<span data-ttu-id="2cb67-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2cb67-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb67-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cb67-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="2cb67-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2cb67-112">Property value</span></span>

<span data-ttu-id="2cb67-113">Devuelve la dirección del nombre para mostrar adaptado para el tipo.</span><span class="sxs-lookup"><span data-stu-id="2cb67-113">returns the address of the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb67-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb67-114">Requirements</span></span>



| <span data-ttu-id="2cb67-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb67-115">Requirement</span></span> | <span data-ttu-id="2cb67-116">Value</span><span class="sxs-lookup"><span data-stu-id="2cb67-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb67-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb67-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cb67-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2cb67-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb67-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="2cb67-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2cb67-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2cb67-121">Redistributable</span></span><br/>          | <span data-ttu-id="2cb67-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="2cb67-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="2cb67-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cb67-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cb67-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb67-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





