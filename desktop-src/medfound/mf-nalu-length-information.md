---
description: Indica las longitudes de NALUs en el ejemplo. Se trata de un BLOB MF que se establece en los ejemplos de entrada comprimidos en el descodificador H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697024"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="52fc2-104">MF \_ Nalu \_ atributo de información de longitud \_</span><span class="sxs-lookup"><span data-stu-id="52fc2-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="52fc2-105">Indica las longitudes de NALUs en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="52fc2-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="52fc2-106">Se trata de un **BLOB** MF que se establece en los ejemplos de entrada comprimidos en el descodificador H. 264.</span><span class="sxs-lookup"><span data-stu-id="52fc2-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="52fc2-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="52fc2-107">Data type</span></span>

<span data-ttu-id="52fc2-108">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="52fc2-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="52fc2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52fc2-109">Remarks</span></span>

<span data-ttu-id="52fc2-110">Para que se establezca este atributo, el medio debe ser de tipo MEDIASUBTYPE \_ H264 y el atributo de [ \_ conjunto de \_ longitud \_ MF Nalu](mf-nalu-length-set.md) debe establecerse en el tipo de medio de entrada de MEDIASUBTYPE \_ H264.</span><span class="sxs-lookup"><span data-stu-id="52fc2-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="52fc2-111">Establezca la \_ información de longitud de MF Nalu \_ \_ como un **BLOB** en el ejemplo de entrada, con un valor DWORD para cada Nalu en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="52fc2-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="52fc2-112">Por ejemplo, si hay 300 000 (9 bytes), SP (25 bytes), PPS (10 bytes), IDR slice1 (50 k), el segmento de IDR 2 (60 k), debe haber 5 DWORD con los valores 9, 25, 10, 50 k, 60 k en el **BLOB**.</span><span class="sxs-lookup"><span data-stu-id="52fc2-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="52fc2-113">Aquí se muestra código que establece el **BLOB**, donde **rgdwNALULengthInfo** es una matriz de tipo DWORD y **uiNaluLengthIdx** es la longitud Nalu válida establecida en el **BLOB**.</span><span class="sxs-lookup"><span data-stu-id="52fc2-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="52fc2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52fc2-114">Requirements</span></span>



| <span data-ttu-id="52fc2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="52fc2-115">Requirement</span></span> | <span data-ttu-id="52fc2-116">Value</span><span class="sxs-lookup"><span data-stu-id="52fc2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52fc2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52fc2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52fc2-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="52fc2-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="52fc2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52fc2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52fc2-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="52fc2-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="52fc2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52fc2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="52fc2-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fc2-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52fc2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="52fc2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fc2-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52fc2-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52fc2-125">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="52fc2-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




