---
title: DRM_PLAY_OPL_EX estructura (wmdrmsdk. h)
description: La estructura de la \_ reproducción \_ de OPL de DRM \_ incluye información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708946"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="bad8f-105">\_Estructura del \_ OPL de reproducción de DRM \_</span><span class="sxs-lookup"><span data-stu-id="bad8f-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="bad8f-106">La estructura de la **\_ reproducción de \_ OPL \_ de DRM** incluye información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bad8f-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad8f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bad8f-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="bad8f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bad8f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bad8f-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="bad8f-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="bad8f-110">Número de versión.</span><span class="sxs-lookup"><span data-stu-id="bad8f-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="bad8f-111">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="bad8f-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="bad8f-112">[**DRM \_ Estructura \_ de \_ \_ niveles de protección de salida mínima**](drmdrm-minimum-output-protection-levels.md) que contiene el OPL mínimo necesario para reproducir contenido en distintos formatos.</span><span class="sxs-lookup"><span data-stu-id="bad8f-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="bad8f-113">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="bad8f-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="bad8f-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bad8f-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="bad8f-115">**vopi**</span><span class="sxs-lookup"><span data-stu-id="bad8f-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="bad8f-116">[**DRM \_ La estructura de \_ \_ \_ IDS de protección de salida de vídeo**](drmdrm-video-output-protection-ids.md) contiene los identificadores de protección de salida de vídeo que se aplican a la reproducción del contenido.</span><span class="sxs-lookup"><span data-stu-id="bad8f-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bad8f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bad8f-117">Remarks</span></span>

<span data-ttu-id="bad8f-118">Esta estructura es idéntica a la estructura del **\_ \_ OPL de reproducción de DRM** , salvo que incluye un número de versión.</span><span class="sxs-lookup"><span data-stu-id="bad8f-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad8f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad8f-119">Requirements</span></span>



| <span data-ttu-id="bad8f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad8f-120">Requirement</span></span> | <span data-ttu-id="bad8f-121">Value</span><span class="sxs-lookup"><span data-stu-id="bad8f-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bad8f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bad8f-122">Header</span></span><br/> | <dl> <span data-ttu-id="bad8f-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad8f-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad8f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bad8f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad8f-125">**el \_ OPL de reproducción de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="bad8f-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="bad8f-126">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="bad8f-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





