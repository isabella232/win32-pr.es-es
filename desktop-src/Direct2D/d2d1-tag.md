---
title: D2D1_TAG (D2d1. h)
description: Un valor de 64 bits definido por la aplicación que se usa para \ 160; marca un conjunto de operaciones de representación.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359713"
---
# <a name="d2d1_tag"></a><span data-ttu-id="11904-104">\_Etiqueta D2D1</span><span class="sxs-lookup"><span data-stu-id="11904-104">D2D1\_TAG</span></span>

<span data-ttu-id="11904-105">Un valor de 64 bits definido por la aplicación que se usa para marcar un conjunto de operaciones de representación.</span><span class="sxs-lookup"><span data-stu-id="11904-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="11904-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11904-106">Remarks</span></span>

<span data-ttu-id="11904-107">Para establecer una etiqueta antes de una serie de operaciones de representación, utilice el método [**ID2D1RenderTarget:: SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="11904-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="11904-108">Para recuperar la etiqueta actual, use el método [**ID2D1RenderTarget:: GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .</span><span class="sxs-lookup"><span data-stu-id="11904-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="11904-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11904-109">Requirements</span></span>



| <span data-ttu-id="11904-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="11904-110">Requirement</span></span> | <span data-ttu-id="11904-111">Value</span><span class="sxs-lookup"><span data-stu-id="11904-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11904-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11904-112">Minimum supported client</span></span><br/> | <span data-ttu-id="11904-113">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="11904-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="11904-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11904-114">Minimum supported server</span></span><br/> | <span data-ttu-id="11904-115">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="11904-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="11904-116">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11904-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="11904-117">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="11904-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="11904-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11904-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="11904-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="11904-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="11904-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="11904-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11904-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="11904-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="11904-122">**SetTags**</span><span class="sxs-lookup"><span data-stu-id="11904-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

