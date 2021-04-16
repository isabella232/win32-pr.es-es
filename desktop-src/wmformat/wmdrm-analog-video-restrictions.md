---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de restricciones de vídeo analógico de WMDRM contiene información sobre una restricción para reproducir el contenido como vídeo analógico.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699528"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="f1156-105">\_Estructura de \_ restricciones de vídeo analógico de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="f1156-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="f1156-106">La estructura de **\_ \_ \_ restricciones de vídeo analógico de WMDRM** contiene información sobre una restricción para reproducir el contenido como vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="f1156-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1156-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1156-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="f1156-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f1156-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1156-109">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="f1156-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="f1156-110">Identificador de restricción.</span><span class="sxs-lookup"><span data-stu-id="f1156-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f1156-111">**dwRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="f1156-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="f1156-112">Datos de restricción.</span><span class="sxs-lookup"><span data-stu-id="f1156-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1156-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1156-113">Remarks</span></span>

<span data-ttu-id="f1156-114">Esta estructura se recibe cuando se llama a [**IWMDRMLicense:: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span><span class="sxs-lookup"><span data-stu-id="f1156-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1156-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1156-115">Requirements</span></span>



| <span data-ttu-id="f1156-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1156-116">Requirement</span></span> | <span data-ttu-id="f1156-117">Value</span><span class="sxs-lookup"><span data-stu-id="f1156-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1156-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1156-118">Header</span></span><br/> | <dl> <span data-ttu-id="f1156-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1156-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1156-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1156-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1156-121">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="f1156-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="f1156-122">**\_restricciones de vídeo analógico de WMDRM \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="f1156-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





