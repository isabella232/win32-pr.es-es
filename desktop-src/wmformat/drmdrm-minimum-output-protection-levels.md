---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS estructura (wmdrmsdk. h)
description: La \_ estructura de \_ niveles de \_ protección de salida mínima de DRM \_ contiene los niveles mínimos de protección de salida (OPLs) para la reproducción de varios tipos de contenido. Un dispositivo debe admitir el valor de OPL mínimo para un tipo de datos para recibir ese tipo de datos del lector.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708206"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="f359c-106">\_Estructura de \_ \_ niveles de protección de salida mínima de DRM \_</span><span class="sxs-lookup"><span data-stu-id="f359c-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="f359c-107">La estructura de **\_ niveles de \_ \_ protección \_ de salida mínima de DRM** contiene los niveles mínimos de protección de salida (OPLs) para la reproducción de varios tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="f359c-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="f359c-108">Un dispositivo debe admitir el valor de OPL mínimo para un tipo de datos para recibir ese tipo de datos del lector.</span><span class="sxs-lookup"><span data-stu-id="f359c-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f359c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f359c-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="f359c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f359c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f359c-111">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="f359c-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="f359c-112">Mínimo de OPL necesario para recibir vídeo digital comprimido.</span><span class="sxs-lookup"><span data-stu-id="f359c-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="f359c-113">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="f359c-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="f359c-114">Mínimo de OPL necesario para recibir vídeo digital no comprimido.</span><span class="sxs-lookup"><span data-stu-id="f359c-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="f359c-115">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="f359c-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="f359c-116">Mínimo de OPL necesario para recibir vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="f359c-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="f359c-117">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="f359c-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="f359c-118">Mínimo de OPL necesario para recibir audio digital comprimido.</span><span class="sxs-lookup"><span data-stu-id="f359c-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="f359c-119">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="f359c-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="f359c-120">Mínimo de OPL necesario para recibir audio digital no comprimido.</span><span class="sxs-lookup"><span data-stu-id="f359c-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f359c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f359c-121">Remarks</span></span>

<span data-ttu-id="f359c-122">Esta estructura se usa como miembro de la estructura [**del \_ \_ OPL de reproducción de DRM**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="f359c-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f359c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f359c-123">Requirements</span></span>



| <span data-ttu-id="f359c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f359c-124">Requirement</span></span> | <span data-ttu-id="f359c-125">Value</span><span class="sxs-lookup"><span data-stu-id="f359c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f359c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f359c-126">Header</span></span><br/> | <dl> <span data-ttu-id="f359c-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f359c-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f359c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f359c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f359c-129">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="f359c-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





