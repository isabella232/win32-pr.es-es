---
title: DownloadItem. Progress
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad Progress recupera el progreso de la descarga en bytes.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- DownloadItem. Progress Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699487"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="93652-106">DownloadItem. Progress</span><span class="sxs-lookup"><span data-stu-id="93652-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="93652-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="93652-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="93652-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="93652-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="93652-109">La propiedad **Progress** recupera el progreso de la descarga en bytes.</span><span class="sxs-lookup"><span data-stu-id="93652-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="93652-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93652-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="93652-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="93652-111">Possible Values</span></span>

<span data-ttu-id="93652-112">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="93652-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="93652-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93652-113">Requirements</span></span>



| <span data-ttu-id="93652-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="93652-114">Requirement</span></span> | <span data-ttu-id="93652-115">Value</span><span class="sxs-lookup"><span data-stu-id="93652-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93652-116">Versión</span><span class="sxs-lookup"><span data-stu-id="93652-116">Version</span></span><br/> | <span data-ttu-id="93652-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="93652-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="93652-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93652-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="93652-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93652-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93652-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="93652-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93652-121">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="93652-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="93652-122">**DownloadItem. Size**</span><span class="sxs-lookup"><span data-stu-id="93652-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 





