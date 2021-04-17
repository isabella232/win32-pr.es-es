---
description: Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits promedio. Esta propiedad se usa junto con la propiedad AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propiedad AVEncCommonMeanBitRateInterval (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495646"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="10abf-104">Propiedad AVEncCommonMeanBitRateInterval</span><span class="sxs-lookup"><span data-stu-id="10abf-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="10abf-105">Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits promedio.</span><span class="sxs-lookup"><span data-stu-id="10abf-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="10abf-106">Esta propiedad se usa junto con la propiedad [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="10abf-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="10abf-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="10abf-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="10abf-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="10abf-108">Data type</span></span>

<span data-ttu-id="10abf-109">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="10abf-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="10abf-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="10abf-110">Property GUID</span></span>

<span data-ttu-id="10abf-111">**CODECAPI \_ AVEncCommonMeanBitRateInterval**</span><span class="sxs-lookup"><span data-stu-id="10abf-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="10abf-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="10abf-112">Property value</span></span>

<span data-ttu-id="10abf-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="10abf-113">This property has a linear range of values.</span></span> <span data-ttu-id="10abf-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="10abf-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="10abf-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10abf-115">Remarks</span></span>

<span data-ttu-id="10abf-116">En el caso de la codificación de velocidad de bits variable (VBR) de dos pasos, el valor cero indica que el intervalo de tiempo es toda la duración del contenido.</span><span class="sxs-lookup"><span data-stu-id="10abf-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="10abf-117">En el caso de la codificación de velocidad de bits constante (CBR) de un solo paso, el valor cero indica que el codificador selecciona el intervalo (normalmente 0,5 segundos).</span><span class="sxs-lookup"><span data-stu-id="10abf-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="10abf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10abf-118">Requirements</span></span>



| <span data-ttu-id="10abf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10abf-119">Requirement</span></span> | <span data-ttu-id="10abf-120">Value</span><span class="sxs-lookup"><span data-stu-id="10abf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10abf-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10abf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10abf-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="10abf-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="10abf-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10abf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10abf-124">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="10abf-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="10abf-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10abf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10abf-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="10abf-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10abf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="10abf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10abf-128">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="10abf-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="10abf-129">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="10abf-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




