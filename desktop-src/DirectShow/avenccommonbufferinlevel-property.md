---
description: Especifica el nivel inicial del búfer de codificación, en bits. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Propiedad AVEncCommonBufferInLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152580"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="cf3fa-104">Propiedad AVEncCommonBufferInLevel</span><span class="sxs-lookup"><span data-stu-id="cf3fa-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="cf3fa-105">Especifica el nivel inicial del búfer de codificación, en bits.</span><span class="sxs-lookup"><span data-stu-id="cf3fa-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="cf3fa-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="cf3fa-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="cf3fa-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cf3fa-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf3fa-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cf3fa-108">Data type</span></span>

<span data-ttu-id="cf3fa-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="cf3fa-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cf3fa-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="cf3fa-110">Property GUID</span></span>

<span data-ttu-id="cf3fa-111">**CODECAPI \_ AVEncCommonBufferInLevel**</span><span class="sxs-lookup"><span data-stu-id="cf3fa-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="cf3fa-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cf3fa-112">Property value</span></span>

<span data-ttu-id="cf3fa-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="cf3fa-113">This property has a linear range of values.</span></span> <span data-ttu-id="cf3fa-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="cf3fa-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf3fa-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf3fa-115">Remarks</span></span>

<span data-ttu-id="cf3fa-116">Para vídeo MPEG, esta propiedad define el llenado inicial del comprobador de búfer de vídeo (VBV).</span><span class="sxs-lookup"><span data-stu-id="cf3fa-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="cf3fa-117">Admite la concatenación de flujos durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="cf3fa-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf3fa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf3fa-118">Requirements</span></span>



| <span data-ttu-id="cf3fa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf3fa-119">Requirement</span></span> | <span data-ttu-id="cf3fa-120">Value</span><span class="sxs-lookup"><span data-stu-id="cf3fa-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3fa-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf3fa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf3fa-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="cf3fa-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cf3fa-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf3fa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf3fa-124">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="cf3fa-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cf3fa-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf3fa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf3fa-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3fa-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3fa-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf3fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3fa-128">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="cf3fa-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cf3fa-129">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cf3fa-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




