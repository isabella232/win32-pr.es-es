---
title: Propiedad DataType de IResultProperty (WdsSharedIDL. h)
description: Un tipo de datos de propiedades.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Propiedad DataType características de entorno de Windows heredadas
- Propiedad DataType características de entorno de Windows heredadas, interfaz IResultProperty
- Interfaz IResultProperty características del entorno heredado de Windows, propiedad DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705155"
---
# <a name="iresultpropertydatatype-property"></a><span data-ttu-id="25983-106">IResultProperty::D propiedad ataType</span><span class="sxs-lookup"><span data-stu-id="25983-106">IResultProperty::DataType property</span></span>

> [!NOTE]
> <span data-ttu-id="25983-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="25983-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="25983-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="25983-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="25983-109">Un tipo de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="25983-109">A properties data type.</span></span>

<span data-ttu-id="25983-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25983-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25983-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25983-111">Syntax</span></span>


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a><span data-ttu-id="25983-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="25983-112">Property value</span></span>

<span data-ttu-id="25983-113">Devuelve un puntero al tipo de datos de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="25983-113">returns a pointer to the properties data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="25983-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25983-114">Requirements</span></span>



| <span data-ttu-id="25983-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25983-115">Requirement</span></span> | <span data-ttu-id="25983-116">Value</span><span class="sxs-lookup"><span data-stu-id="25983-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="25983-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25983-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25983-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25983-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="25983-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25983-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25983-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="25983-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25983-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="25983-121">Redistributable</span></span><br/>          | <span data-ttu-id="25983-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="25983-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="25983-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25983-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25983-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="25983-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





