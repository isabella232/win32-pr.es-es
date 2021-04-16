---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX estructura (wmdrmsdk. h)
description: La \_ \_ estructura de los ID. de protección de la salida de audio DRM \_ \_ \_ contiene una lista de identificadores de protección de salida de audio. Esta estructura extiende los \_ \_ \_ identificadores de protección de salida de audio DRM \_ agregando un número de versión.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718964"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="674a1-106">\_Estructura de \_ los \_ \_ identificadores \_ de salida de audio DRM</span><span class="sxs-lookup"><span data-stu-id="674a1-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="674a1-107">La estructura de los ID. de protección de la **\_ salida de audio \_ \_ \_ \_ DRM** contiene una lista de identificadores de protección de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="674a1-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="674a1-108">Esta estructura extiende **los \_ \_ \_ \_ identificadores de protección de salida de audio DRM** agregando un número de versión.</span><span class="sxs-lookup"><span data-stu-id="674a1-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="674a1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="674a1-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="674a1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="674a1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="674a1-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="674a1-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="674a1-112">Número de versión.</span><span class="sxs-lookup"><span data-stu-id="674a1-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="674a1-113">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="674a1-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="674a1-114">Número de entradas de la matriz **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="674a1-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="674a1-115">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="674a1-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="674a1-116">Matriz de **estructuras \_ \_ ex de \_ protección \_ de salida de audio DRM** .</span><span class="sxs-lookup"><span data-stu-id="674a1-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="674a1-117">**DRM \_ La \_ protección de salida de audio \_ \_ ex** es un tipo definido como [**protección de \_ salida DRM \_ \_ ex**](drm-output-protection-ex.md).</span><span class="sxs-lookup"><span data-stu-id="674a1-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="674a1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="674a1-118">Remarks</span></span>

<span data-ttu-id="674a1-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="674a1-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="674a1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="674a1-120">Requirements</span></span>



| <span data-ttu-id="674a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="674a1-121">Requirement</span></span> | <span data-ttu-id="674a1-122">Value</span><span class="sxs-lookup"><span data-stu-id="674a1-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="674a1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="674a1-123">Header</span></span><br/> | <dl> <span data-ttu-id="674a1-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="674a1-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674a1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="674a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674a1-126">**\_ \_ \_ identificadores de protección de salida de audio DRM \_**</span><span class="sxs-lookup"><span data-stu-id="674a1-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="674a1-127">**\_ \_ \_ identificadores de protección de salida de \_ vídeo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="674a1-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="674a1-128">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="674a1-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





