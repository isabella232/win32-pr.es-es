---
description: El método SWbemRefresher. DeleteAll quita todos los elementos de la colección en el objeto SWbemRefresher. Objeto SWbemRefresher.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Método SWbemRefresher. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707555"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="e1d0d-103">SWbemRefresher. DeleteAll, método</span><span class="sxs-lookup"><span data-stu-id="e1d0d-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="e1d0d-104">El método **SWbemRefresher. deleteAll** quita todos los elementos de la colección en el objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d0d-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="e1d0d-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e1d0d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1d0d-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="e1d0d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1d0d-107">Parameters</span></span>

<span data-ttu-id="e1d0d-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1d0d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1d0d-109">Return value</span></span>

<span data-ttu-id="e1d0d-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d0d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1d0d-111">Remarks</span></span>

<span data-ttu-id="e1d0d-112">El [**SWbemRefreshableItem**](swbemrefreshableitem.md) correspondiente para cada elemento quitado tiene su propiedad [**actualizador**](swbemrefreshableitem-refresher.md) establecida en **null**, lo que indica que ya no tiene un actualizador primario.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d0d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d0d-113">Requirements</span></span>



| <span data-ttu-id="e1d0d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d0d-114">Requirement</span></span> | <span data-ttu-id="e1d0d-115">Value</span><span class="sxs-lookup"><span data-stu-id="e1d0d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d0d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1d0d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d0d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1d0d-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1d0d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1d0d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d0d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1d0d-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1d0d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1d0d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1d0d-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d0d-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1d0d-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e1d0d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1d0d-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e1d0d-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e1d0d-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1d0d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1d0d-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d0d-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1d0d-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="e1d0d-126">CLSID</span></span><br/>                    | <span data-ttu-id="e1d0d-127">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="e1d0d-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="e1d0d-128">IID</span><span class="sxs-lookup"><span data-stu-id="e1d0d-128">IID</span></span><br/>                      | <span data-ttu-id="e1d0d-129">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="e1d0d-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="e1d0d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1d0d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d0d-131">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="e1d0d-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




