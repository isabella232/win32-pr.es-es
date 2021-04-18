---
title: DRM_PLAY_OPL estructura (wmdrmsdk. h)
description: La estructura del OPL de reproducción de DRM \_ \_ contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700370"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="d0b3c-105">Estructura del OPL de \_ reproducción de DRM \_</span><span class="sxs-lookup"><span data-stu-id="d0b3c-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="d0b3c-106">La estructura del **\_ \_ OPL de reproducción de DRM** contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d0b3c-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b3c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b3c-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="d0b3c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0b3c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0b3c-109">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="d0b3c-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="d0b3c-110">[**DRM \_ Estructura \_ de \_ \_ niveles de protección de salida mínima**](drmdrm-minimum-output-protection-levels.md) que contiene el OPL mínimo necesario para reproducir contenido en distintos formatos.</span><span class="sxs-lookup"><span data-stu-id="d0b3c-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="d0b3c-111">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="d0b3c-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="d0b3c-112">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d0b3c-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d0b3c-113">**vopi**</span><span class="sxs-lookup"><span data-stu-id="d0b3c-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="d0b3c-114">[**DRM \_ La estructura de \_ \_ \_ IDS de protección de salida de vídeo**](drmdrm-video-output-protection-ids.md) contiene los identificadores de protección de salida de vídeo que se aplican a la reproducción del contenido.</span><span class="sxs-lookup"><span data-stu-id="d0b3c-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0b3c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b3c-115">Requirements</span></span>



| <span data-ttu-id="d0b3c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b3c-116">Requirement</span></span> | <span data-ttu-id="d0b3c-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0b3c-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b3c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0b3c-118">Header</span></span><br/> | <dl> <span data-ttu-id="d0b3c-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b3c-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b3c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b3c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b3c-121">**el \_ OPL de copia de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="d0b3c-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="d0b3c-122">**el \_ OPL de reproducción de DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="d0b3c-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="d0b3c-123">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="d0b3c-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





