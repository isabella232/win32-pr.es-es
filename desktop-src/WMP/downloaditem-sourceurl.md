---
title: DownloadItem.sourceURL
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad sourceURL recupera la dirección URL de origen de la descarga.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- DownloadItem. sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699595"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="1c2c1-106">DownloadItem.sourceURL</span><span class="sxs-lookup"><span data-stu-id="1c2c1-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="1c2c1-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="1c2c1-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1c2c1-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1c2c1-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1c2c1-109">La propiedad **sourceURL** recupera la dirección URL de origen de la descarga.</span><span class="sxs-lookup"><span data-stu-id="1c2c1-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2c1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c2c1-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="1c2c1-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1c2c1-111">Possible Values</span></span>

<span data-ttu-id="1c2c1-112">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1c2c1-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c2c1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c2c1-113">Remarks</span></span>

<span data-ttu-id="1c2c1-114">Solo se pueden descargar los siguientes formatos de medios digitales:</span><span class="sxs-lookup"><span data-stu-id="1c2c1-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="1c2c1-115">Formato ASF</span><span class="sxs-lookup"><span data-stu-id="1c2c1-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="1c2c1-116">MP3</span><span class="sxs-lookup"><span data-stu-id="1c2c1-116">MP3</span></span>
-   <span data-ttu-id="1c2c1-117">Audio de Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="1c2c1-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="1c2c1-118">Vídeo de Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="1c2c1-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2c1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c2c1-119">Requirements</span></span>



| <span data-ttu-id="1c2c1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c2c1-120">Requirement</span></span> | <span data-ttu-id="1c2c1-121">Value</span><span class="sxs-lookup"><span data-stu-id="1c2c1-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2c1-122">Versión</span><span class="sxs-lookup"><span data-stu-id="1c2c1-122">Version</span></span><br/> | <span data-ttu-id="1c2c1-123">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="1c2c1-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1c2c1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c2c1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c2c1-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c2c1-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c2c1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c2c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2c1-127">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="1c2c1-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





