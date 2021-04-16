---
description: La interfaz IKsPin proporciona un método para recuperar los medios admitidos por un PIN en un filtro de modo kernel. IKsPin tiene métodos adicionales además del que se muestra aquí, pero no se admiten para DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interfaz IKsPin (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677116"
---
# <a name="ikspin-interface"></a><span data-ttu-id="52ad6-104">Interfaz IKsPin</span><span class="sxs-lookup"><span data-stu-id="52ad6-104">IKsPin interface</span></span>

<span data-ttu-id="52ad6-105">La `IKsPin` interfaz proporciona un método para recuperar los medios admitidos por un PIN en un filtro de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="52ad6-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="52ad6-106">`IKsPin` tiene métodos adicionales además del que se muestra aquí, pero no se admiten para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="52ad6-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="52ad6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="52ad6-107">Members</span></span>

<span data-ttu-id="52ad6-108">La interfaz **IKsPin** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="52ad6-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="52ad6-109">**IKsPin** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="52ad6-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="52ad6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="52ad6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52ad6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="52ad6-111">Methods</span></span>

<span data-ttu-id="52ad6-112">La interfaz **IKsPin** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="52ad6-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="52ad6-113">Método</span><span class="sxs-lookup"><span data-stu-id="52ad6-113">Method</span></span>                                          | <span data-ttu-id="52ad6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="52ad6-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="52ad6-115">**KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="52ad6-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="52ad6-116">Recupera los medios admitidos por un PIN.</span><span class="sxs-lookup"><span data-stu-id="52ad6-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52ad6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52ad6-117">Remarks</span></span>

<span data-ttu-id="52ad6-118">Debe incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="52ad6-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="52ad6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52ad6-119">Requirements</span></span>



| <span data-ttu-id="52ad6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ad6-120">Requirement</span></span> | <span data-ttu-id="52ad6-121">Value</span><span class="sxs-lookup"><span data-stu-id="52ad6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52ad6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52ad6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52ad6-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52ad6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="52ad6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52ad6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52ad6-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52ad6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52ad6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52ad6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ad6-127"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ad6-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="52ad6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52ad6-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="52ad6-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52ad6-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
