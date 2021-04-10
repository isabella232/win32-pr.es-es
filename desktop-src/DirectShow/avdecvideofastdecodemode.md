---
description: Obtiene o establece la velocidad de descodificación de vídeo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propiedad AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152584"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="010ff-103">Propiedad AVDecVideoFastDecodeMode</span><span class="sxs-lookup"><span data-stu-id="010ff-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="010ff-104">Obtiene o establece la velocidad de descodificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="010ff-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="010ff-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="010ff-105">Data type</span></span>

<span data-ttu-id="010ff-106">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="010ff-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="010ff-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="010ff-107">Property GUID</span></span>

<span data-ttu-id="010ff-108">**CODECAPI \_ AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="010ff-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="010ff-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="010ff-109">Property value</span></span>

<span data-ttu-id="010ff-110">El valor de esta propiedad puede oscilar entre 0 y 32, donde 0 indica descodificación normal y 32 es el modo de descodificación más rápido.</span><span class="sxs-lookup"><span data-stu-id="010ff-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="010ff-111">El comportamiento exacto depende de la implementación del descodificador.</span><span class="sxs-lookup"><span data-stu-id="010ff-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="010ff-112">No todos los incrementos entre 1 y 32 que define necesariamente es un modo distinto.</span><span class="sxs-lookup"><span data-stu-id="010ff-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="010ff-113">La enumeración [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contiene algunos modos predefinidos para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="010ff-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="010ff-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="010ff-114">Requirements</span></span>



| <span data-ttu-id="010ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="010ff-115">Requirement</span></span> | <span data-ttu-id="010ff-116">Value</span><span class="sxs-lookup"><span data-stu-id="010ff-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="010ff-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="010ff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="010ff-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="010ff-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="010ff-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="010ff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="010ff-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="010ff-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="010ff-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="010ff-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="010ff-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="010ff-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010ff-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="010ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010ff-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="010ff-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="010ff-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="010ff-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




