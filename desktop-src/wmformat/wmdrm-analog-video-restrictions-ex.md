---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX estructura (wmdrmsdk. h)
description: La \_ \_ \_ \_ estructura de restricciones de vídeo analógico de WMDRM contiene información amplia sobre una restricción para reproducir el contenido como vídeo analógico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699529"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="cd334-105">\_Restricciones de vídeo analógico de WMDRM ( \_ \_ \_ estructura)</span><span class="sxs-lookup"><span data-stu-id="cd334-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="cd334-106">La estructura de **\_ \_ \_ restricciones de \_ vídeo analógico de WMDRM** contiene información amplia sobre una restricción para reproducir el contenido como vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="cd334-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd334-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd334-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="cd334-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd334-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd334-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="cd334-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="cd334-110">Número de versión.</span><span class="sxs-lookup"><span data-stu-id="cd334-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="cd334-111">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="cd334-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="cd334-112">IDENTIFICADOR de restricción.</span><span class="sxs-lookup"><span data-stu-id="cd334-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="cd334-113">**cbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="cd334-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="cd334-114">Tamaño de los datos de restricción en bytes.</span><span class="sxs-lookup"><span data-stu-id="cd334-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cd334-115">**pbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="cd334-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="cd334-116">Datos de restricción.</span><span class="sxs-lookup"><span data-stu-id="cd334-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd334-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd334-117">Remarks</span></span>

<span data-ttu-id="cd334-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd334-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd334-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd334-119">Requirements</span></span>



| <span data-ttu-id="cd334-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd334-120">Requirement</span></span> | <span data-ttu-id="cd334-121">Value</span><span class="sxs-lookup"><span data-stu-id="cd334-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd334-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd334-122">Header</span></span><br/> | <dl> <span data-ttu-id="cd334-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd334-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd334-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd334-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd334-125">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="cd334-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="cd334-126">**\_restricciones de \_ vídeo \_ analógico de WMDRM**</span><span class="sxs-lookup"><span data-stu-id="cd334-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





