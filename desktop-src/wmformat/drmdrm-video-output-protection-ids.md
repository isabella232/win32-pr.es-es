---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de IDS de protección de vídeo de DRM \_ contiene una matriz de \_ estructuras de protección de salida de vídeo DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708205"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="ed4ca-105">\_Estructura de \_ IDS de protección de salida de vídeo DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed4ca-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="ed4ca-106">La estructura de **\_ \_ \_ \_ IDS de protección de vídeo de DRM** contiene una matriz de estructuras de **\_ \_ \_ protección de salida de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="ed4ca-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed4ca-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="ed4ca-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ed4ca-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed4ca-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="ed4ca-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="ed4ca-110">Número de elementos de la matriz a los que hace referencia **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="ed4ca-111">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="ed4ca-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="ed4ca-112">Dirección de una matriz de estructuras de **\_ protección de \_ salida \_ de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="ed4ca-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="ed4ca-113">**DRM \_ La \_ \_ protección de salida de vídeo** es un tipo definido como [**\_ \_ protección de salida de DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="ed4ca-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed4ca-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed4ca-114">Remarks</span></span>

<span data-ttu-id="ed4ca-115">Esta estructura se usa como miembro de la estructura [**del \_ \_ OPL de reproducción de DRM**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4ca-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4ca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed4ca-116">Requirements</span></span>



| <span data-ttu-id="ed4ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed4ca-117">Requirement</span></span> | <span data-ttu-id="ed4ca-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed4ca-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4ca-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed4ca-119">Header</span></span><br/> | <dl> <span data-ttu-id="ed4ca-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed4ca-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4ca-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed4ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4ca-122">**\_ \_ \_ identificadores de protección de salida de audio DRM \_**</span><span class="sxs-lookup"><span data-stu-id="ed4ca-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="ed4ca-123">**\_ \_ \_ identificadores de protección de salida de \_ vídeo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="ed4ca-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="ed4ca-124">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="ed4ca-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





