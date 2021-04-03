---
description: Habilita o deshabilita la ecualización de sonoridad en un descodificador de audio o en un procesador de señal digital (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propiedad AVDSPLoudnessEqualization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997993"
---
# <a name="avdsploudnessequalization-property"></a><span data-ttu-id="dce2a-103">Propiedad AVDSPLoudnessEqualization</span><span class="sxs-lookup"><span data-stu-id="dce2a-103">AVDSPLoudnessEqualization property</span></span>

<span data-ttu-id="dce2a-104">Habilita o deshabilita la ecualización de sonoridad en un descodificador de audio o en un procesador de señal digital (DSP).</span><span class="sxs-lookup"><span data-stu-id="dce2a-104">Enables or disables loudness equalization in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="dce2a-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dce2a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="dce2a-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dce2a-106">Data type</span></span>

<span data-ttu-id="dce2a-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="dce2a-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="dce2a-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="dce2a-108">Property GUID</span></span>

<span data-ttu-id="dce2a-109">**CODECAPI \_ AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="dce2a-109">**CODECAPI\_AVDSPLoudnessEqualization**</span></span>

## <a name="property-value"></a><span data-ttu-id="dce2a-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dce2a-110">Property value</span></span>

<span data-ttu-id="dce2a-111">El valor de esta propiedad es un miembro de la enumeración [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .</span><span class="sxs-lookup"><span data-stu-id="dce2a-111">The value of this property is a member of the [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce2a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dce2a-112">Remarks</span></span>

<span data-ttu-id="dce2a-113">La ecualización de sonoridad es un proceso de DSP que mantiene un nivel de volumen coherente cuando cambia la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="dce2a-113">Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce2a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dce2a-114">Requirements</span></span>



| <span data-ttu-id="dce2a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce2a-115">Requirement</span></span> | <span data-ttu-id="dce2a-116">Value</span><span class="sxs-lookup"><span data-stu-id="dce2a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dce2a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dce2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dce2a-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="dce2a-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="dce2a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dce2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dce2a-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="dce2a-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="dce2a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dce2a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce2a-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce2a-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce2a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="dce2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce2a-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="dce2a-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="dce2a-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="dce2a-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




