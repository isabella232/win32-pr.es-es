---
title: DownloadItem. Cancel (método)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método CANCEL cancela la descarga.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancelar el método Media Player de Windows
- método CANCEL Windows Media Player, clase DownloadItem
- Clase DownloadItem Windows Media Player, método CANCEL
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700084"
---
# <a name="downloaditemcancel-method"></a><span data-ttu-id="5358d-108">DownloadItem. Cancel (método)</span><span class="sxs-lookup"><span data-stu-id="5358d-108">DownloadItem.cancel method</span></span>

> [!Note]  
> <span data-ttu-id="5358d-109">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="5358d-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5358d-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5358d-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5358d-111">El método **Cancel** cancela la descarga.</span><span class="sxs-lookup"><span data-stu-id="5358d-111">The **cancel** method cancels the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="5358d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5358d-112">Syntax</span></span>


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a><span data-ttu-id="5358d-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5358d-113">Parameters</span></span>

<span data-ttu-id="5358d-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5358d-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5358d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5358d-115">Return value</span></span>

<span data-ttu-id="5358d-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5358d-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5358d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5358d-117">Remarks</span></span>

<span data-ttu-id="5358d-118">Los elementos cancelados no se quitan de la colección de descargas.</span><span class="sxs-lookup"><span data-stu-id="5358d-118">Cancelled items are not removed from the download collection.</span></span> <span data-ttu-id="5358d-119">Los elementos cancelados devuelven un valor de **downloadState** de 4 (cancelado).</span><span class="sxs-lookup"><span data-stu-id="5358d-119">Cancelled items return a **downloadState** value of 4 (canceled).</span></span>

## <a name="requirements"></a><span data-ttu-id="5358d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5358d-120">Requirements</span></span>



| <span data-ttu-id="5358d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5358d-121">Requirement</span></span> | <span data-ttu-id="5358d-122">Value</span><span class="sxs-lookup"><span data-stu-id="5358d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5358d-123">Versión</span><span class="sxs-lookup"><span data-stu-id="5358d-123">Version</span></span><br/> | <span data-ttu-id="5358d-124">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="5358d-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5358d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5358d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5358d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5358d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5358d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5358d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5358d-128">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="5358d-128">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="5358d-129">**DownloadItem.downloadState**</span><span class="sxs-lookup"><span data-stu-id="5358d-129">**DownloadItem.downloadState**</span></span>](downloaditem-downloadstate.md)
</dt> </dl>

 

 





