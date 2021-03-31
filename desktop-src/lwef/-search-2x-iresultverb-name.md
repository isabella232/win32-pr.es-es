---
title: Propiedad nombre de IResultVerb (WdsSharedIDL. h)
description: Esta propiedad devuelve un puntero al nombre de cononical para el verbo, como imprimir, abrir, etc.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Propiedad nombre características heredadas del entorno de Windows
- Propiedad nombre características de entorno heredado de Windows, interfaz IResultVerb
- Interfaz IResultVerb características del entorno heredado de Windows, propiedad Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995987"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="e8270-106">IResultVerb:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e8270-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="e8270-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e8270-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e8270-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e8270-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e8270-109">Esta propiedad devuelve un puntero al nombre de cononical para el verbo, como imprimir, abrir, etc.</span><span class="sxs-lookup"><span data-stu-id="e8270-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="e8270-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8270-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8270-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8270-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="e8270-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8270-112">Property value</span></span>

<span data-ttu-id="e8270-113">Name es un puntero al nombre de cononical para el verbo.</span><span class="sxs-lookup"><span data-stu-id="e8270-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8270-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8270-114">Requirements</span></span>



| <span data-ttu-id="e8270-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8270-115">Requirement</span></span> | <span data-ttu-id="e8270-116">Value</span><span class="sxs-lookup"><span data-stu-id="e8270-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8270-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8270-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8270-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8270-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e8270-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8270-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8270-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="e8270-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e8270-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e8270-121">Redistributable</span></span><br/>          | <span data-ttu-id="e8270-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e8270-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="e8270-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8270-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8270-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8270-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





