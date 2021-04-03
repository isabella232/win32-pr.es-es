---
description: Especifica la precisión de los coeficientes del controlador de dominio, en bits. Esta propiedad se aplica a los codificadores de vídeo MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Propiedad AVEncMPVIntraDCPrecision (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906688"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="b6c79-104">Propiedad AVEncMPVIntraDCPrecision</span><span class="sxs-lookup"><span data-stu-id="b6c79-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="b6c79-105">Especifica la precisión de los coeficientes del controlador de dominio, en bits.</span><span class="sxs-lookup"><span data-stu-id="b6c79-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="b6c79-106">Esta propiedad se aplica a los codificadores de vídeo MPEG.</span><span class="sxs-lookup"><span data-stu-id="b6c79-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="b6c79-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b6c79-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6c79-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b6c79-108">Data type</span></span>

<span data-ttu-id="b6c79-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b6c79-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b6c79-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="b6c79-110">Property GUID</span></span>

<span data-ttu-id="b6c79-111">**CODECAPI \_ AVEncMPVIntraDCPrecision**</span><span class="sxs-lookup"><span data-stu-id="b6c79-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="b6c79-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b6c79-112">Property value</span></span>

<span data-ttu-id="b6c79-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="b6c79-113">This property has a linear range of values.</span></span> <span data-ttu-id="b6c79-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="b6c79-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c79-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6c79-115">Remarks</span></span>

<span data-ttu-id="b6c79-116">El intervalo habitual de esta propiedad es de 8 a 11 bits.</span><span class="sxs-lookup"><span data-stu-id="b6c79-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="b6c79-117">Si el valor es cero, el codificador selecciona la precisión.</span><span class="sxs-lookup"><span data-stu-id="b6c79-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c79-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c79-118">Requirements</span></span>



| <span data-ttu-id="b6c79-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c79-119">Requirement</span></span> | <span data-ttu-id="b6c79-120">Value</span><span class="sxs-lookup"><span data-stu-id="b6c79-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c79-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6c79-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c79-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="b6c79-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b6c79-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6c79-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c79-124">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="b6c79-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b6c79-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6c79-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6c79-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c79-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c79-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6c79-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c79-128">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="b6c79-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b6c79-129">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b6c79-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




