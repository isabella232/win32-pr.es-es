---
title: Propiedad UID de IResultType (WdsSharedIDL. h)
description: Esta propiedad contiene el identificador único para el tipo.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- Propiedad UID características de entorno heredado de Windows
- Propiedad UID características de entorno heredado de Windows, interfaz IResultType
- Interfaz IResultType características del entorno heredado de Windows, propiedad UID
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151160"
---
# <a name="iresulttypeuid-property"></a><span data-ttu-id="80337-106">IResultType:: UID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="80337-106">IResultType::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="80337-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="80337-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="80337-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="80337-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="80337-109">Esta propiedad contiene el identificador único para el tipo.</span><span class="sxs-lookup"><span data-stu-id="80337-109">This property contains the unique identifier for the type.</span></span>

<span data-ttu-id="80337-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80337-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80337-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80337-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="80337-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="80337-112">Property value</span></span>

<span data-ttu-id="80337-113">Dirección de la ubicación que contiene el UID.</span><span class="sxs-lookup"><span data-stu-id="80337-113">the address of the location containing the uid.</span></span>

## <a name="requirements"></a><span data-ttu-id="80337-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80337-114">Requirements</span></span>



| <span data-ttu-id="80337-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="80337-115">Requirement</span></span> | <span data-ttu-id="80337-116">Value</span><span class="sxs-lookup"><span data-stu-id="80337-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80337-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80337-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80337-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="80337-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="80337-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80337-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80337-120">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="80337-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80337-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="80337-121">Redistributable</span></span><br/>          | <span data-ttu-id="80337-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="80337-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="80337-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80337-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="80337-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="80337-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





