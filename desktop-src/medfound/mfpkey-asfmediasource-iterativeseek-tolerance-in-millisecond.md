---
description: Establece la tolerancia, en milisegundos, que se utiliza cuando el origen de medios ASF realiza búsquedas iterativas.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Propiedad MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697952"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="bc18f-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerancia \_ en \_ milisegundos</span><span class="sxs-lookup"><span data-stu-id="bc18f-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="bc18f-104">Establece la tolerancia, en milisegundos, que se utiliza cuando el origen de medios ASF realiza búsquedas iterativas.</span><span class="sxs-lookup"><span data-stu-id="bc18f-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="bc18f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bc18f-105">Data type</span></span>

<span data-ttu-id="bc18f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="bc18f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bc18f-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="bc18f-107">PROPVARIANT member</span></span>

<span data-ttu-id="bc18f-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="bc18f-108">**ULONG**</span></span>

<span data-ttu-id="bc18f-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bc18f-109">VT\_UI4</span></span>

<span data-ttu-id="bc18f-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="bc18f-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bc18f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc18f-111">Remarks</span></span>

<span data-ttu-id="bc18f-112">Utilice esta propiedad para configurar el origen de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="bc18f-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="bc18f-113">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="bc18f-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bc18f-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bc18f-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="bc18f-115">Esta propiedad solo se aplica cuando está habilitada la búsqueda iterativa.</span><span class="sxs-lookup"><span data-stu-id="bc18f-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="bc18f-116">Para obtener más información, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="bc18f-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="bc18f-117">El algoritmo de búsqueda iterativa se detiene si encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada.</span><span class="sxs-lookup"><span data-stu-id="bc18f-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="bc18f-118">El valor predeterminado es 8000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="bc18f-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc18f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc18f-119">Requirements</span></span>



| <span data-ttu-id="bc18f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc18f-120">Requirement</span></span> | <span data-ttu-id="bc18f-121">Value</span><span class="sxs-lookup"><span data-stu-id="bc18f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc18f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc18f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc18f-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bc18f-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bc18f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc18f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc18f-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="bc18f-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bc18f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc18f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc18f-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc18f-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc18f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc18f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc18f-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc18f-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




