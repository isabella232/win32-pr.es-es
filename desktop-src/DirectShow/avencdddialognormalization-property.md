---
description: Especifica el nivel de normalización del cuadro de diálogo, en decibelios (dB), en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Propiedad AVEncDDDialogNormalization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495623"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="11e8a-104">Propiedad AVEncDDDialogNormalization</span><span class="sxs-lookup"><span data-stu-id="11e8a-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="11e8a-105">Especifica el nivel de normalización del cuadro de diálogo, en decibelios (dB), en una secuencia de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="11e8a-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="11e8a-106">Esta propiedad se aplica a los codificadores de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="11e8a-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="11e8a-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="11e8a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="11e8a-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="11e8a-108">Data type</span></span>

<span data-ttu-id="11e8a-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="11e8a-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="11e8a-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="11e8a-110">Property GUID</span></span>

<span data-ttu-id="11e8a-111">**CODECAPI \_ AVEncDDDialogNormalization**</span><span class="sxs-lookup"><span data-stu-id="11e8a-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="11e8a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="11e8a-112">Property value</span></span>

<span data-ttu-id="11e8a-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="11e8a-113">This property has a linear range of values.</span></span> <span data-ttu-id="11e8a-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="11e8a-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="11e8a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11e8a-115">Requirements</span></span>



| <span data-ttu-id="11e8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e8a-116">Requirement</span></span> | <span data-ttu-id="11e8a-117">Value</span><span class="sxs-lookup"><span data-stu-id="11e8a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11e8a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11e8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11e8a-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="11e8a-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="11e8a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11e8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11e8a-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="11e8a-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="11e8a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11e8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e8a-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e8a-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e8a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="11e8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e8a-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="11e8a-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="11e8a-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="11e8a-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




