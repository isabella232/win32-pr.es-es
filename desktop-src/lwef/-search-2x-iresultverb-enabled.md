---
title: Propiedad habilitada para IResultVerb (WdsSharedIDL. h)
description: Esta propiedad devuelve TRUE si el verbo está habilitado.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Características habilitadas para el entorno de Windows heredado de propiedades
- Propiedad habilitada características del entorno de Windows heredado, interfaz IResultVerb
- Interfaz IResultVerb características del entorno heredado de Windows, propiedad habilitada
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996664"
---
# <a name="iresultverbenabled-property"></a><span data-ttu-id="61e35-106">IResultVerb:: Enabled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="61e35-106">IResultVerb::Enabled property</span></span>

> [!NOTE]
> <span data-ttu-id="61e35-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61e35-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="61e35-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="61e35-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="61e35-109">Esta propiedad devuelve TRUE si el verbo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="61e35-109">This property returns TRUE if the verb is enabled.</span></span>

<span data-ttu-id="61e35-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="61e35-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e35-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61e35-111">Syntax</span></span>


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a><span data-ttu-id="61e35-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="61e35-112">Property value</span></span>

<span data-ttu-id="61e35-113">Esta propiedad devuelve true si el verbo está habilitado o false si no lo está.</span><span class="sxs-lookup"><span data-stu-id="61e35-113">This property returns True if the verb is enabled or False if not.</span></span>

## <a name="requirements"></a><span data-ttu-id="61e35-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61e35-114">Requirements</span></span>



| <span data-ttu-id="61e35-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="61e35-115">Requirement</span></span> | <span data-ttu-id="61e35-116">Value</span><span class="sxs-lookup"><span data-stu-id="61e35-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e35-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61e35-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61e35-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="61e35-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="61e35-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61e35-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61e35-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="61e35-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61e35-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="61e35-121">Redistributable</span></span><br/>          | <span data-ttu-id="61e35-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="61e35-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="61e35-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61e35-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61e35-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="61e35-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





