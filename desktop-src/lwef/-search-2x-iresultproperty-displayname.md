---
title: Propiedad IResultProperty DisplayName (WdsSharedIDL. h)
description: Nombre para mostrar localizado de la propiedad.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultProperty
- Interfaz IResultProperty características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150577"
---
# <a name="iresultpropertydisplayname-property"></a><span data-ttu-id="0183d-106">IResultProperty::D propiedad isplayName</span><span class="sxs-lookup"><span data-stu-id="0183d-106">IResultProperty::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="0183d-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0183d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0183d-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0183d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0183d-109">Nombre para mostrar localizado de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0183d-109">Localized display name of the property.</span></span>

<span data-ttu-id="0183d-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0183d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0183d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0183d-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="0183d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0183d-112">Property value</span></span>

<span data-ttu-id="0183d-113">Devuelve un puntero al nombre para mostrar localizado.</span><span class="sxs-lookup"><span data-stu-id="0183d-113">returns a pointer to the localized display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="0183d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0183d-114">Requirements</span></span>



| <span data-ttu-id="0183d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0183d-115">Requirement</span></span> | <span data-ttu-id="0183d-116">Value</span><span class="sxs-lookup"><span data-stu-id="0183d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0183d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0183d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0183d-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0183d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0183d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0183d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0183d-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="0183d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0183d-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0183d-121">Redistributable</span></span><br/>          | <span data-ttu-id="0183d-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="0183d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="0183d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0183d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0183d-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0183d-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





