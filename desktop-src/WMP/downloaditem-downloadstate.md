---
title: DownloadItem.downloadState
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad downloadState recupera el estado de la descarga.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadState Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700346"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="5b9be-106">DownloadItem.downloadState</span><span class="sxs-lookup"><span data-stu-id="5b9be-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="5b9be-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="5b9be-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5b9be-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5b9be-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5b9be-109">La propiedad **downloadState** recupera el estado de la descarga.</span><span class="sxs-lookup"><span data-stu-id="5b9be-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b9be-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b9be-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="5b9be-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5b9be-111">Possible Values</span></span>

<span data-ttu-id="5b9be-112">Esta propiedad es un **número** de solo lectura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b9be-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="5b9be-113">Value</span><span class="sxs-lookup"><span data-stu-id="5b9be-113">Value</span></span> | <span data-ttu-id="5b9be-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b9be-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5b9be-115">0</span><span class="sxs-lookup"><span data-stu-id="5b9be-115">0</span></span>     | <span data-ttu-id="5b9be-116">Downloading (Descargando)</span><span class="sxs-lookup"><span data-stu-id="5b9be-116">Downloading</span></span> |
| <span data-ttu-id="5b9be-117">1</span><span class="sxs-lookup"><span data-stu-id="5b9be-117">1</span></span>     | <span data-ttu-id="5b9be-118">En pausa</span><span class="sxs-lookup"><span data-stu-id="5b9be-118">Paused</span></span>      |
| <span data-ttu-id="5b9be-119">2</span><span class="sxs-lookup"><span data-stu-id="5b9be-119">2</span></span>     | <span data-ttu-id="5b9be-120">Processing</span><span class="sxs-lookup"><span data-stu-id="5b9be-120">Processing</span></span>  |
| <span data-ttu-id="5b9be-121">3</span><span class="sxs-lookup"><span data-stu-id="5b9be-121">3</span></span>     | <span data-ttu-id="5b9be-122">Completado</span><span class="sxs-lookup"><span data-stu-id="5b9be-122">Completed</span></span>   |
| <span data-ttu-id="5b9be-123">4</span><span class="sxs-lookup"><span data-stu-id="5b9be-123">4</span></span>     | <span data-ttu-id="5b9be-124">Canceled</span><span class="sxs-lookup"><span data-stu-id="5b9be-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="5b9be-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b9be-125">Remarks</span></span>

<span data-ttu-id="5b9be-126">Los Estados de descarga se pueden producir en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="5b9be-126">Download states can occur in any order.</span></span> <span data-ttu-id="5b9be-127">No Escriba código que dependa de la aparición de un estado de descarga determinado.</span><span class="sxs-lookup"><span data-stu-id="5b9be-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b9be-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b9be-128">Requirements</span></span>



| <span data-ttu-id="5b9be-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b9be-129">Requirement</span></span> | <span data-ttu-id="5b9be-130">Value</span><span class="sxs-lookup"><span data-stu-id="5b9be-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9be-131">Versión</span><span class="sxs-lookup"><span data-stu-id="5b9be-131">Version</span></span><br/> | <span data-ttu-id="5b9be-132">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="5b9be-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="5b9be-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b9be-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b9be-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b9be-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b9be-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b9be-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b9be-136">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="5b9be-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





