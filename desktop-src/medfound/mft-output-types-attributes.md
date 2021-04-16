---
description: Contiene los tipos de salida registrados para una transformación de Media Foundation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705898"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="91ea7-103">\_Atributo de \_ atributos de tipos de salida de MFT \_</span><span class="sxs-lookup"><span data-stu-id="91ea7-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="91ea7-104">Contiene los tipos de salida registrados para una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="91ea7-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="91ea7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="91ea7-105">Data type</span></span>

<span data-ttu-id="91ea7-106">**MFT \_ Registrar \_ \_ información \[ de \] tipo** almacenada como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="91ea7-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="91ea7-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91ea7-107">Remarks</span></span>

<span data-ttu-id="91ea7-108">Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="91ea7-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="91ea7-109">Este atributo contiene una matriz de estructuras de información de tipo de registro de MFT que describen uno o más formatos de salida admitidos por la MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)</span><span class="sxs-lookup"><span data-stu-id="91ea7-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="91ea7-110">Estos valores se toman del registro y están pensados como una sugerencia para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91ea7-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="91ea7-111">La MFT podría admitir formatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="91ea7-111">The MFT might support additional formats.</span></span> <span data-ttu-id="91ea7-112">Para establecer el formato de salida real, debe crear la MFT y llamar a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="91ea7-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="91ea7-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="91ea7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ea7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ea7-114">Requirements</span></span>



| <span data-ttu-id="91ea7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ea7-115">Requirement</span></span> | <span data-ttu-id="91ea7-116">Value</span><span class="sxs-lookup"><span data-stu-id="91ea7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ea7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91ea7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91ea7-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="91ea7-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="91ea7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91ea7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91ea7-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="91ea7-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="91ea7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91ea7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ea7-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="91ea7-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ea7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="91ea7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ea7-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91ea7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91ea7-125">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="91ea7-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




