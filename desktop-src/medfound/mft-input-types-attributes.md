---
description: Contiene los tipos de entrada registrados para una transformación de Media Foundation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: MFT_INPUT_TYPES_Attributes atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543915"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="293c4-103">\_Atributo de \_ atributos de tipos de entrada de MFT \_</span><span class="sxs-lookup"><span data-stu-id="293c4-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="293c4-104">Contiene los tipos de entrada registrados para una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="293c4-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="293c4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="293c4-105">Data type</span></span>

<span data-ttu-id="293c4-106">**MFT \_ Registrar \_ \_ información \[ de \] tipo** almacenada como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="293c4-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="293c4-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="293c4-107">Get/set</span></span>

<span data-ttu-id="293c4-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="293c4-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="293c4-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="293c4-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="293c4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="293c4-110">Remarks</span></span>

<span data-ttu-id="293c4-111">Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="293c4-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="293c4-112">Este atributo contiene una matriz de estructuras de información de tipo de registro de MFT que describen uno o más formatos de entrada admitidos por la MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)</span><span class="sxs-lookup"><span data-stu-id="293c4-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="293c4-113">Estos valores se toman del registro y están pensados como una sugerencia para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="293c4-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="293c4-114">La MFT podría admitir formatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="293c4-114">The MFT might support additional formats.</span></span> <span data-ttu-id="293c4-115">Para establecer el formato de entrada real, debe crear la MFT y llamar a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="293c4-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="293c4-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="293c4-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="293c4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="293c4-117">Requirements</span></span>



| <span data-ttu-id="293c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="293c4-118">Requirement</span></span> | <span data-ttu-id="293c4-119">Value</span><span class="sxs-lookup"><span data-stu-id="293c4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="293c4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="293c4-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="293c4-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="293c4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="293c4-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="293c4-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="293c4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="293c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="293c4-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="293c4-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293c4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="293c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293c4-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="293c4-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="293c4-128">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="293c4-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




