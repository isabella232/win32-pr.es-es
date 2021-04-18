---
title: DownloadItem. Size
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad Size recupera el tamaño de la descarga.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem. Size Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699747"
---
# <a name="downloaditemsize"></a><span data-ttu-id="b4c3c-106">DownloadItem. Size</span><span class="sxs-lookup"><span data-stu-id="b4c3c-106">DownloadItem.size</span></span>

> [!Note]  
> <span data-ttu-id="b4c3c-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="b4c3c-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b4c3c-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="b4c3c-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b4c3c-109">La propiedad **size** recupera el tamaño de la descarga.</span><span class="sxs-lookup"><span data-stu-id="b4c3c-109">The **size** property retrieves the size of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c3c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4c3c-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a><span data-ttu-id="b4c3c-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="b4c3c-111">Possible Values</span></span>

<span data-ttu-id="b4c3c-112">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="b4c3c-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c3c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4c3c-113">Requirements</span></span>



| <span data-ttu-id="b4c3c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c3c-114">Requirement</span></span> | <span data-ttu-id="b4c3c-115">Value</span><span class="sxs-lookup"><span data-stu-id="b4c3c-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c3c-116">Versión</span><span class="sxs-lookup"><span data-stu-id="b4c3c-116">Version</span></span><br/> | <span data-ttu-id="b4c3c-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b4c3c-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="b4c3c-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4c3c-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4c3c-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4c3c-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c3c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4c3c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c3c-121">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="b4c3c-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="b4c3c-122">**DownloadItem. Progress**</span><span class="sxs-lookup"><span data-stu-id="b4c3c-122">**DownloadItem.progress**</span></span>](downloaditem-progress.md)
</dt> </dl>

 

 





