---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS estructura (wmdrmsdk. h)
description: La \_ \_ \_ \_ estructura de ID. de protección de salida de audio DRM contiene una lista de identificadores de protección de salida de audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718963"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="44aff-105">\_Estructura de \_ IDS de protección de salida de audio DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="44aff-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="44aff-106">La estructura de ID. de **\_ protección de salida de audio \_ \_ \_ DRM** contiene una lista de identificadores de protección de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="44aff-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="44aff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44aff-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="44aff-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="44aff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="44aff-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="44aff-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="44aff-110">Número de entradas de la matriz **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="44aff-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="44aff-111">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="44aff-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="44aff-112">Matriz de estructuras de **\_ protección de \_ salida \_ de audio DRM** .</span><span class="sxs-lookup"><span data-stu-id="44aff-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="44aff-113">**DRM \_ La \_ \_ protección de salida de audio** es un tipo definido como [**\_ \_ protección de salida de DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="44aff-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44aff-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44aff-114">Remarks</span></span>

<span data-ttu-id="44aff-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44aff-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="44aff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44aff-116">Requirements</span></span>



| <span data-ttu-id="44aff-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="44aff-117">Requirement</span></span> | <span data-ttu-id="44aff-118">Value</span><span class="sxs-lookup"><span data-stu-id="44aff-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44aff-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44aff-119">Header</span></span><br/> | <dl> <span data-ttu-id="44aff-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="44aff-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44aff-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="44aff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44aff-122">**\_ \_ \_ identificadores de protección de salida de \_ audio DRM \_**</span><span class="sxs-lookup"><span data-stu-id="44aff-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="44aff-123">**\_ \_ \_ identificadores de protección de salida de vídeo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="44aff-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="44aff-124">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="44aff-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





