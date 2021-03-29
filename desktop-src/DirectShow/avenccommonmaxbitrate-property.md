---
description: Especifica la velocidad de bits máxima, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Propiedad AVEncCommonMaxBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906793"
---
# <a name="avenccommonmaxbitrate-property"></a><span data-ttu-id="7e9c2-104">Propiedad AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="7e9c2-104">AVEncCommonMaxBitRate property</span></span>

<span data-ttu-id="7e9c2-105">Especifica la velocidad de bits máxima, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="7e9c2-105">Specifies the maximum bit rate, in bits per second.</span></span> <span data-ttu-id="7e9c2-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="7e9c2-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="7e9c2-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7e9c2-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e9c2-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7e9c2-108">Data type</span></span>

<span data-ttu-id="7e9c2-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7e9c2-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7e9c2-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e9c2-110">Property GUID</span></span>

<span data-ttu-id="7e9c2-111">**CODECAPI \_ AVEncCommonMaxBitRate**</span><span class="sxs-lookup"><span data-stu-id="7e9c2-111">**CODECAPI\_AVEncCommonMaxBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="7e9c2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e9c2-112">Property value</span></span>

<span data-ttu-id="7e9c2-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="7e9c2-113">This property has a linear range of values.</span></span> <span data-ttu-id="7e9c2-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="7e9c2-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9c2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9c2-115">Requirements</span></span>



| <span data-ttu-id="7e9c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9c2-116">Requirement</span></span> | <span data-ttu-id="7e9c2-117">Value</span><span class="sxs-lookup"><span data-stu-id="7e9c2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9c2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e9c2-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="7e9c2-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7e9c2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e9c2-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="7e9c2-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7e9c2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e9c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e9c2-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e9c2-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e9c2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e9c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9c2-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="7e9c2-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7e9c2-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7e9c2-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




