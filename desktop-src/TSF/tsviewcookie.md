---
title: TsViewCookie (Textstor. h)
description: El tipo de datos TsViewCookie identifica una vista de contexto.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685913"
---
# <a name="tsviewcookie"></a><span data-ttu-id="5249d-104">TsViewCookie</span><span class="sxs-lookup"><span data-stu-id="5249d-104">TsViewCookie</span></span>

<span data-ttu-id="5249d-105">El tipo de datos **TsViewCookie** identifica una vista de contexto.</span><span class="sxs-lookup"><span data-stu-id="5249d-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="5249d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5249d-106">Remarks</span></span>

<span data-ttu-id="5249d-107">Una aplicación debe proporcionar un valor de **TsViewCookie** único para cada vista que cree.</span><span class="sxs-lookup"><span data-stu-id="5249d-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="5249d-108">El administrador de TSF obtiene este valor de la aplicación mediante una llamada a [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) o [ITextStoreAnchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span><span class="sxs-lookup"><span data-stu-id="5249d-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="5249d-109">El administrador de TSF usa este valor para identificar la vista cuando se llama a varios métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) o [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="5249d-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="5249d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5249d-110">Requirements</span></span>



| <span data-ttu-id="5249d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5249d-111">Requirement</span></span> | <span data-ttu-id="5249d-112">Value</span><span class="sxs-lookup"><span data-stu-id="5249d-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5249d-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5249d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5249d-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="5249d-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="5249d-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5249d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5249d-116">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="5249d-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="5249d-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5249d-117">Redistributable</span></span><br/>          | <span data-ttu-id="5249d-118">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5249d-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="5249d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5249d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5249d-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="5249d-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="5249d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="5249d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5249d-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5249d-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5249d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5249d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5249d-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="5249d-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="5249d-125">**ITextStoreACP:: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="5249d-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="5249d-126">**ITextStoreAnchor::GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="5249d-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





