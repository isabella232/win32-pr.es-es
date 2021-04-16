---
description: Especifica la velocidad de bits mínima, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Propiedad AVEncCommonMinBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686404"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="90ea5-104">Propiedad AVEncCommonMinBitRate</span><span class="sxs-lookup"><span data-stu-id="90ea5-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="90ea5-105">Especifica la velocidad de bits mínima, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="90ea5-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="90ea5-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="90ea5-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="90ea5-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="90ea5-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="90ea5-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="90ea5-108">Data type</span></span>

<span data-ttu-id="90ea5-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="90ea5-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="90ea5-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="90ea5-110">Property GUID</span></span>

<span data-ttu-id="90ea5-111">**CODECAPI \_ AVEncCommonMinBitRate**</span><span class="sxs-lookup"><span data-stu-id="90ea5-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="90ea5-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="90ea5-112">Property value</span></span>

<span data-ttu-id="90ea5-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="90ea5-113">This property has a linear range of values.</span></span> <span data-ttu-id="90ea5-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="90ea5-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="90ea5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90ea5-115">Remarks</span></span>

<span data-ttu-id="90ea5-116">El codificador aplica la velocidad de bits mínima al aumentar la calidad de la codificación según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="90ea5-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ea5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90ea5-117">Requirements</span></span>



| <span data-ttu-id="90ea5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ea5-118">Requirement</span></span> | <span data-ttu-id="90ea5-119">Value</span><span class="sxs-lookup"><span data-stu-id="90ea5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90ea5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ea5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="90ea5-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="90ea5-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="90ea5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ea5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="90ea5-123">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="90ea5-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="90ea5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90ea5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ea5-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ea5-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ea5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="90ea5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ea5-127">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="90ea5-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="90ea5-128">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="90ea5-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




