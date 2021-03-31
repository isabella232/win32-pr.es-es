---
description: Especifica el &\# 0034; depósito de fugas&\# 0034; parámetros de una secuencia en un receptor de medios ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Propiedad MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908143"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="ecfb7-103">\_ \_ Propiedad LEAKYBUCKET corregida ASFSTREAMSINK MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="ecfb7-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="ecfb7-104">Especifica los parámetros de "depósito de fugas" (vea la sección comentarios) de una secuencia en un receptor de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="ecfb7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ecfb7-105">Data type</span></span>

<span data-ttu-id="ecfb7-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="ecfb7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ecfb7-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="ecfb7-107">PROPVARIANT member</span></span>

<span data-ttu-id="ecfb7-108">Matriz de valores **DWORD** (**caul**)</span><span class="sxs-lookup"><span data-stu-id="ecfb7-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="ecfb7-109">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ecfb7-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="ecfb7-110">**caul**</span><span class="sxs-lookup"><span data-stu-id="ecfb7-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="ecfb7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecfb7-111">Remarks</span></span>

<span data-ttu-id="ecfb7-112">Una aplicación puede establecer esta propiedad en una secuencia del receptor de medios ASF una vez negociado el tipo de medio para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="ecfb7-113">Utilice esta propiedad para especificar la ventana de búfer real que utilizará el códec de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="ecfb7-114">Puede obtener esta información del códec mediante la interfaz **IWMCodecLeakyBucket** , que se documenta en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="ecfb7-115">El valor de esta propiedad es una matriz de tres valores **DWORD** en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="ecfb7-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="ecfb7-116">Velocidad de bits, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="ecfb7-117">Tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="ecfb7-118">Llenado inicial del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ecfb7-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecfb7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecfb7-119">Requirements</span></span>



| <span data-ttu-id="ecfb7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecfb7-120">Requirement</span></span> | <span data-ttu-id="ecfb7-121">Value</span><span class="sxs-lookup"><span data-stu-id="ecfb7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecfb7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ecfb7-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecfb7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ecfb7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecfb7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ecfb7-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecfb7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ecfb7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecfb7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecfb7-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb7-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecfb7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecfb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecfb7-129">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="ecfb7-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="ecfb7-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecfb7-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




