---
description: Contiene marcas para un objeto de activación de transformación de Media Foundation (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: MF_TRANSFORM_FLAGS_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001358"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="462ee-103">MF \_ Transform \_ \_ attributes atributo Attribute</span><span class="sxs-lookup"><span data-stu-id="462ee-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="462ee-104">Contiene marcas para un objeto de activación de transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="462ee-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="462ee-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="462ee-105">Data type</span></span>

<span data-ttu-id="462ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="462ee-106">**UINT32**</span></span>

<span data-ttu-id="462ee-107">El valor es **una operación OR** bit a bit de marcas de la enumeración de la [**\_ \_ \_ marca de enumeración MFT**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) .</span><span class="sxs-lookup"><span data-stu-id="462ee-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="462ee-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="462ee-108">Get/set</span></span>

<span data-ttu-id="462ee-109">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="462ee-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="462ee-110">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="462ee-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="462ee-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="462ee-111">Remarks</span></span>

<span data-ttu-id="462ee-112">Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="462ee-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="462ee-113">El atributo contiene marcas que describen la MFT.</span><span class="sxs-lookup"><span data-stu-id="462ee-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="462ee-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="462ee-114">Requirements</span></span>



| <span data-ttu-id="462ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="462ee-115">Requirement</span></span> | <span data-ttu-id="462ee-116">Value</span><span class="sxs-lookup"><span data-stu-id="462ee-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="462ee-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="462ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="462ee-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="462ee-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="462ee-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="462ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="462ee-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="462ee-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="462ee-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="462ee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="462ee-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="462ee-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="462ee-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="462ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462ee-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="462ee-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="462ee-125">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="462ee-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
