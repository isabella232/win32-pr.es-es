---
description: Configura el origen de medios ASF para usar búsquedas iterativas si el archivo de origen no tiene ningún índice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Propiedad MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820287"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="17dfd-103">\_ \_ Propiedad ITERATIVESEEKIFNOINDEX de MFPKEY ASFMediaSource</span><span class="sxs-lookup"><span data-stu-id="17dfd-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="17dfd-104">Configura el origen de medios ASF para usar búsquedas iterativas si el archivo de origen no tiene ningún índice.</span><span class="sxs-lookup"><span data-stu-id="17dfd-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="17dfd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="17dfd-105">Data type</span></span>

<span data-ttu-id="17dfd-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="17dfd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="17dfd-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="17dfd-107">PROPVARIANT member</span></span>

<span data-ttu-id="17dfd-108">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="17dfd-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="17dfd-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="17dfd-109">VT\_BOOL</span></span>

<span data-ttu-id="17dfd-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="17dfd-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="17dfd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17dfd-111">Remarks</span></span>

<span data-ttu-id="17dfd-112">Utilice esta propiedad para configurar el origen de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="17dfd-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="17dfd-113">Para establecer la propiedad, pase un puntero **IPropertyStore** a la *resolución de origen*.</span><span class="sxs-lookup"><span data-stu-id="17dfd-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="17dfd-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="17dfd-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="17dfd-115">La *búsqueda iterativa* es un algoritmo para encontrar una posición en un archivo ASF sin índice.</span><span class="sxs-lookup"><span data-stu-id="17dfd-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="17dfd-116">Usa una serie de aproximaciones, en función de la velocidad de bits media, para que se acerquen progresivamente al tiempo de búsqueda del destino.</span><span class="sxs-lookup"><span data-stu-id="17dfd-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="17dfd-117">(El algoritmo es similar a una búsqueda binaria). La búsqueda iterativa puede tardar más que la búsqueda por índice, por lo que está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17dfd-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="17dfd-118">Si establece esta propiedad, use las siguientes propiedades para establecer los parámetros de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="17dfd-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="17dfd-119">Recuento máximo de MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_</span><span class="sxs-lookup"><span data-stu-id="17dfd-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="17dfd-120">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerancia \_ en \_ milisegundos</span><span class="sxs-lookup"><span data-stu-id="17dfd-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="17dfd-121">Estas propiedades establecen el número máximo de iteraciones y la tolerancia, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="17dfd-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="17dfd-122">El algoritmo se detiene cuando alcanza el número máximo de iteraciones o cuando encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada.</span><span class="sxs-lookup"><span data-stu-id="17dfd-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="17dfd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dfd-123">Requirements</span></span>



| <span data-ttu-id="17dfd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="17dfd-124">Requirement</span></span> | <span data-ttu-id="17dfd-125">Value</span><span class="sxs-lookup"><span data-stu-id="17dfd-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17dfd-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dfd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="17dfd-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="17dfd-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="17dfd-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dfd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="17dfd-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="17dfd-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="17dfd-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17dfd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="17dfd-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17dfd-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17dfd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="17dfd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17dfd-133">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17dfd-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




