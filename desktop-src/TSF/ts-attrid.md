---
title: TS_ATTRID (Textstor. h)
description: El \_ tipo de datos ATTRID de TS se usa para identificar un atributo de texto.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800986"
---
# <a name="ts_attrid"></a><span data-ttu-id="82822-104">ATTRID de TS \_</span><span class="sxs-lookup"><span data-stu-id="82822-104">TS\_ATTRID</span></span>

<span data-ttu-id="82822-105">El tipo de datos **\_ ATTRID de TS** se usa para identificar un atributo de texto.</span><span class="sxs-lookup"><span data-stu-id="82822-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="82822-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82822-106">Remarks</span></span>

<span data-ttu-id="82822-107">Una lista de GUID predefinidos para ATTRID de TS \_ está en tsattrs. h.</span><span class="sxs-lookup"><span data-stu-id="82822-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="82822-108">Los GUID TSATTRID \_ Text \_ VERTICALWRITING y TSATTRID \_ Text \_ Orientation son útiles para que las aplicaciones coincidan con el texto de entrada que se va a corregir.</span><span class="sxs-lookup"><span data-stu-id="82822-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="82822-109">Se pueden crear GUID adicionales definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="82822-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="82822-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82822-110">Requirements</span></span>



| <span data-ttu-id="82822-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="82822-111">Requirement</span></span> | <span data-ttu-id="82822-112">Value</span><span class="sxs-lookup"><span data-stu-id="82822-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82822-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82822-113">Minimum supported client</span></span><br/> | <span data-ttu-id="82822-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="82822-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="82822-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82822-115">Minimum supported server</span></span><br/> | <span data-ttu-id="82822-116">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="82822-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="82822-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="82822-117">Redistributable</span></span><br/>          | <span data-ttu-id="82822-118">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82822-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="82822-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82822-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="82822-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="82822-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="82822-121">IDL</span><span class="sxs-lookup"><span data-stu-id="82822-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82822-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82822-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82822-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="82822-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82822-124">**ITextStoreACP:: FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="82822-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="82822-125">**ITextStoreACP:: RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="82822-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="82822-126">**ITextStoreACP:: RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="82822-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="82822-127">**ITextStoreACP:: RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="82822-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="82822-128">**ITextStoreACPSink::OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="82822-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="82822-129">**ITextStoreAnchor::FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="82822-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="82822-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="82822-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="82822-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="82822-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="82822-132">**ITextStoreAnchor::RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="82822-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="82822-133">**ITextStoreAnchorSink::OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="82822-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="82822-134">**ATTRVAL de TS \_**</span><span class="sxs-lookup"><span data-stu-id="82822-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





