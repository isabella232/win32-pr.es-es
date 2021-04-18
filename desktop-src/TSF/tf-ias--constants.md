---
title: Constantes de TF_IAS_ (msctf. h)
description: Las constantes de TF \_ IAS \_ \ se utilizan como marcas de bits en métodos que insertan texto o objetos incrustados en una selección o un punto de inserción.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685968"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="1fb2c-103">TF \_ IAS ( \_ \* constantes)</span><span class="sxs-lookup"><span data-stu-id="1fb2c-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="1fb2c-104">Las constantes de TF \_ IAS \_ \* se utilizan como marcas de bits en métodos que insertan texto o objetos incrustados en una selección o un punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="1fb2c-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="1fb2c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1fb2c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fb2c-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="1fb2c-107"><dt>**TF \_ \_NOquery de IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2c-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="1fb2c-108">Se inserta texto y el puntero de intervalo se establece en **null** al salir.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="1fb2c-109">No se puede combinar con la \_ marca TF IAS \_ QUERYONLY.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="1fb2c-110"><dt>**TF \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2c-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="1fb2c-111">No realice la inserción.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-111">Do not perform the insert.</span></span> <span data-ttu-id="1fb2c-112">El autor de la llamada solo requiere que se establezca el puntero de intervalo.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="1fb2c-113">No se puede combinar con la \_ marca TF IAS \_ noquery.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="1fb2c-114"><dt>**TF \_ \_No hay \_ ninguna \_ composición predeterminada de IAS**</dt> <dt>(0x80000000)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2c-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="1fb2c-115">TSF no creará una composición predeterminada si se requiere una composición.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="1fb2c-116">El autor de la llamada debe iniciar una composición en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="1fb2c-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="1fb2c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb2c-117">Requirements</span></span>



| <span data-ttu-id="1fb2c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb2c-118">Requirement</span></span> | <span data-ttu-id="1fb2c-119">Value</span><span class="sxs-lookup"><span data-stu-id="1fb2c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb2c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fb2c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb2c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1fb2c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1fb2c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fb2c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb2c-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fb2c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1fb2c-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1fb2c-124">Redistributable</span></span><br/>          | <span data-ttu-id="1fb2c-125">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1fb2c-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="1fb2c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fb2c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fb2c-127"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2c-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fb2c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="1fb2c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fb2c-129"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2c-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb2c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fb2c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb2c-131">ITextStoreACP:: InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="1fb2c-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="1fb2c-132">ITextStoreACP:: InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="1fb2c-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="1fb2c-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="1fb2c-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="1fb2c-134">ITextStoreAnchor::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="1fb2c-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="1fb2c-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="1fb2c-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="1fb2c-136">ITfInsertAtSelection::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="1fb2c-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





