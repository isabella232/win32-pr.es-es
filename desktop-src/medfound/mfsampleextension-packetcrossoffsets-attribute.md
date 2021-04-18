---
description: Especifica los desplazamientos de los límites de carga en un marco para los ejemplos protegidos.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: MFSampleExtension_PacketCrossOffsets atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720445"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="15678-103">\_Atributo PacketCrossOffsets de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="15678-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="15678-104">Especifica los desplazamientos de los límites de carga en un marco para los ejemplos protegidos.</span><span class="sxs-lookup"><span data-stu-id="15678-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="15678-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="15678-105">Data type</span></span>

<span data-ttu-id="15678-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="15678-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="15678-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="15678-107">Get/set</span></span>

<span data-ttu-id="15678-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="15678-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="15678-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="15678-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="15678-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="15678-110">Applies to</span></span>

[<span data-ttu-id="15678-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="15678-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="15678-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15678-112">Remarks</span></span>

<span data-ttu-id="15678-113">Este atributo se aplica a los ejemplos de medios protegidos por Rights Management digital (DRM) de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="15678-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="15678-114">El valor del atributo es una matriz de **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="15678-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="15678-115">Cada entrada de la matriz es el desplazamiento de un límite de carga, con respecto al inicio del marco.</span><span class="sxs-lookup"><span data-stu-id="15678-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="15678-116">Una aplicación puede utilizar estos valores al descifrar y reconstruir los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="15678-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="15678-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="15678-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="15678-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15678-118">Requirements</span></span>



| <span data-ttu-id="15678-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15678-119">Requirement</span></span> | <span data-ttu-id="15678-120">Value</span><span class="sxs-lookup"><span data-stu-id="15678-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15678-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15678-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15678-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="15678-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="15678-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15678-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15678-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="15678-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="15678-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15678-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15678-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="15678-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15678-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="15678-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15678-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15678-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15678-129">Divisor ASF</span><span class="sxs-lookup"><span data-stu-id="15678-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="15678-130">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="15678-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="15678-131">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="15678-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




