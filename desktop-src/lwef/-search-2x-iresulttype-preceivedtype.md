---
title: Propiedad IResultType PreceivedType (WdsSharedIDL. h)
description: Esta propiedad contiene la cadena que se usa para identificar el tipo en el índice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Propiedad PreceivedType características de entorno heredado de Windows
- Propiedad PreceivedType características de entorno heredado de Windows, interfaz IResultType
- Interfaz IResultType características del entorno heredado de Windows, propiedad PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905144"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="838d3-106">IResultType::P propiedad receivedType</span><span class="sxs-lookup"><span data-stu-id="838d3-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="838d3-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="838d3-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="838d3-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="838d3-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="838d3-109">Esta propiedad contiene la cadena que se usa para identificar el tipo en el índice.</span><span class="sxs-lookup"><span data-stu-id="838d3-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="838d3-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="838d3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="838d3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="838d3-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="838d3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="838d3-112">Property value</span></span>

<span data-ttu-id="838d3-113">Devuelve la dirección de la cadena identifyint tipo en el índice.</span><span class="sxs-lookup"><span data-stu-id="838d3-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="838d3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="838d3-114">Requirements</span></span>



| <span data-ttu-id="838d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="838d3-115">Requirement</span></span> | <span data-ttu-id="838d3-116">Value</span><span class="sxs-lookup"><span data-stu-id="838d3-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="838d3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="838d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="838d3-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="838d3-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="838d3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="838d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="838d3-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="838d3-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="838d3-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="838d3-121">Redistributable</span></span><br/>          | <span data-ttu-id="838d3-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="838d3-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="838d3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="838d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="838d3-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="838d3-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





