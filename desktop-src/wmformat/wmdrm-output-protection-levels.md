---
title: WMDRM_OUTPUT_PROTECTION_LEVELS estructura (wmdrmsdk. h)
description: La estructura de niveles de protección de salida de WMDRM \_ \_ \_ contiene los niveles de protección de salida (OPLs) requeridos por una licencia para realizar varias acciones.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718714"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="a786f-105">\_Estructura de \_ niveles de protección de salida WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="a786f-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="a786f-106">La estructura de niveles de protección de salida de WMDRM contiene los niveles de protección de salida (OPLs) requeridos por una licencia para realizar varias acciones. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a786f-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a786f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a786f-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="a786f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a786f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a786f-109">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="a786f-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="a786f-110">Mínimo de OPL necesario para recibir vídeo digital comprimido.</span><span class="sxs-lookup"><span data-stu-id="a786f-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="a786f-111">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="a786f-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="a786f-112">Mínimo de OPL necesario para recibir vídeo digital no comprimido.</span><span class="sxs-lookup"><span data-stu-id="a786f-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="a786f-113">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="a786f-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="a786f-114">Mínimo de OPL necesario para recibir vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="a786f-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="a786f-115">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="a786f-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="a786f-116">Mínimo de OPL necesario para recibir audio digital comprimido.</span><span class="sxs-lookup"><span data-stu-id="a786f-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="a786f-117">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="a786f-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="a786f-118">Mínimo de OPL necesario para recibir audio digital no comprimido.</span><span class="sxs-lookup"><span data-stu-id="a786f-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="a786f-119">**wMinimumCopyProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="a786f-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="a786f-120">Mínimo de OPL necesario para copiar el contenido.</span><span class="sxs-lookup"><span data-stu-id="a786f-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a786f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a786f-121">Remarks</span></span>

<span data-ttu-id="a786f-122">El método [**IWMDRMLicense:: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="a786f-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a786f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a786f-123">Requirements</span></span>



| <span data-ttu-id="a786f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a786f-124">Requirement</span></span> | <span data-ttu-id="a786f-125">Value</span><span class="sxs-lookup"><span data-stu-id="a786f-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a786f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a786f-126">Header</span></span><br/> | <dl> <span data-ttu-id="a786f-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a786f-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a786f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a786f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a786f-129">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="a786f-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





