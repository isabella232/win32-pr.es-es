---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX estructura (wmdrmsdk. h)
description: La \_ \_ \_ \_ estructura de ID. de protección de salida de vídeo DRM \_ contiene una matriz de \_ estructuras de protección de salida de vídeo DRM \_ \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708142"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="e48a1-105">\_Estructura de \_ los \_ \_ identificadores \_ de salida de vídeo DRM</span><span class="sxs-lookup"><span data-stu-id="e48a1-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="e48a1-106">La estructura de ID. de **\_ protección de salida de vídeo \_ \_ \_ \_ DRM** contiene una matriz de estructuras de **protección de \_ \_ salida \_ de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="e48a1-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e48a1-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="e48a1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e48a1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e48a1-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="e48a1-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e48a1-110">Número de versión.</span><span class="sxs-lookup"><span data-stu-id="e48a1-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="e48a1-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="e48a1-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e48a1-112">Número de elementos de la matriz a los que hace referencia **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="e48a1-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="e48a1-113">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="e48a1-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="e48a1-114">Dirección de una matriz de estructuras de **\_ protección de salida de vídeo \_ \_ \_ DRM** .</span><span class="sxs-lookup"><span data-stu-id="e48a1-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="e48a1-115">**DRM \_ Protección de salida de vídeo: por \_ \_ \_ ejemplo** , un tipo definido como [**protección de \_ salida DRM \_ \_ ex**](drm-output-protection-ex.md).</span><span class="sxs-lookup"><span data-stu-id="e48a1-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e48a1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e48a1-116">Remarks</span></span>

<span data-ttu-id="e48a1-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e48a1-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e48a1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e48a1-118">Requirements</span></span>



| <span data-ttu-id="e48a1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e48a1-119">Requirement</span></span> | <span data-ttu-id="e48a1-120">Value</span><span class="sxs-lookup"><span data-stu-id="e48a1-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e48a1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e48a1-121">Header</span></span><br/> | <dl> <span data-ttu-id="e48a1-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48a1-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48a1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e48a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48a1-124">**\_ \_ \_ identificadores de protección de salida de \_ audio DRM \_**</span><span class="sxs-lookup"><span data-stu-id="e48a1-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="e48a1-125">**\_ \_ \_ identificadores de protección de salida de vídeo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="e48a1-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="e48a1-126">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="e48a1-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





