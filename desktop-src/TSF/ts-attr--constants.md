---
title: Constantes de TS_ATTR_ (Textstor. h)
description: '\_Se usan las constantes de TS ATTR \_ \ para obtener y cambiar los valores de los atributos del documento. Estas constantes forman los valores posibles de las marcas de campo de bits en los métodos ITextStoreACP y ITextStoreAnchor.'
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491890"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="41145-104">\_Constantes de atributo de TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="41145-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="41145-105">Las \_ constantes ATTR \_ \* de TS se utilizan para obtener y cambiar los valores de los atributos del documento.</span><span class="sxs-lookup"><span data-stu-id="41145-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="41145-106">Estas constantes forman los valores posibles de las marcas de campo de bits en los métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) y [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="41145-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="41145-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="41145-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="41145-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="41145-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="41145-109"><dt>**TS \_ ATTR \_ Buscar \_ hacia atrás**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="41145-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="41145-110">Buscar hacia atrás desde el carácter inicial o la posición del delimitador para la posición en la que se produce una transición en un valor de atributo del documento.</span><span class="sxs-lookup"><span data-stu-id="41145-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="41145-111">El valor predeterminado es buscar hacia delante.</span><span class="sxs-lookup"><span data-stu-id="41145-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="41145-112"><dt>**TS \_ ATRIBUTO \_ busque \_ el \_ desplazamiento deseado**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="41145-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="41145-113">Devuelve el número de caracteres entre el carácter de inicio o la posición del delimitador (**acpStart** en [ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) o en el **Inicio** en [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) y la posición en la que se produce la transición de un atributo.</span><span class="sxs-lookup"><span data-stu-id="41145-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="41145-114"><dt>**TS \_ ATTR \_ Buscar \_ UPDATESTART**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="41145-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="41145-115">Lo usa [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) para colocar el delimitador de entrada en la siguiente transición de atributo, si se encuentra uno.</span><span class="sxs-lookup"><span data-stu-id="41145-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="41145-116">De lo contrario, el delimitador de entrada no se modifica.</span><span class="sxs-lookup"><span data-stu-id="41145-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="41145-117"><dt>**TS \_ ATTR \_ Buscar \_ \_ valor deseado**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="41145-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="41145-118">Cargar los valores de atributo de documento admitidos en la estructura [ \_ ATTRVAL de TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .</span><span class="sxs-lookup"><span data-stu-id="41145-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="41145-119"><dt>**TS \_ ATTR \_ Buscar \_ desea \_ Finalizar**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="41145-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="41145-120">Lo usa [ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) y [ITextStoreAnchor:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) para obtener los valores de atributo del documento que terminan en el carácter o posición delimitador especificados.</span><span class="sxs-lookup"><span data-stu-id="41145-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="41145-121"><dt>**TS \_ ATTR \_ Buscar \_ oculto**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="41145-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="41145-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="41145-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="41145-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41145-123">Requirements</span></span>



| <span data-ttu-id="41145-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="41145-124">Requirement</span></span> | <span data-ttu-id="41145-125">Value</span><span class="sxs-lookup"><span data-stu-id="41145-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41145-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41145-126">Minimum supported client</span></span><br/> | <span data-ttu-id="41145-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41145-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="41145-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41145-128">Minimum supported server</span></span><br/> | <span data-ttu-id="41145-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41145-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41145-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="41145-130">Redistributable</span></span><br/>          | <span data-ttu-id="41145-131">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41145-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="41145-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41145-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="41145-133"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="41145-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="41145-134">IDL</span><span class="sxs-lookup"><span data-stu-id="41145-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41145-135"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41145-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41145-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="41145-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41145-137">ATTRID de TS \_</span><span class="sxs-lookup"><span data-stu-id="41145-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="41145-138">ATTRVAL de TS \_</span><span class="sxs-lookup"><span data-stu-id="41145-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="41145-139">ITextStoreACP:: FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="41145-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="41145-140">ITextStoreACP:: RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="41145-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="41145-141">ITextStoreAnchor::FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="41145-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="41145-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="41145-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





