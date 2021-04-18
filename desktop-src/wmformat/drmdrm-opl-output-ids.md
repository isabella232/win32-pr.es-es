---
title: DRM_OPL_OUTPUT_IDS estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de los ID. de salida del OPL de DRM contiene varios identificadores de salida de nivel de protección de salida (OPL).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709012"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="a9a5e-105">Estructura de IDS. de \_ salida de DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9a5e-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="a9a5e-106">La estructura de los ID. de salida del OPL de DRM contiene varios identificadores de salida de nivel de protección de salida (OPL). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9a5e-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a5e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9a5e-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="a9a5e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9a5e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9a5e-109">**Cid**</span><span class="sxs-lookup"><span data-stu-id="a9a5e-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="a9a5e-110">Número de identificadores de la matriz a los que hace referencia **rgIds**.</span><span class="sxs-lookup"><span data-stu-id="a9a5e-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="a9a5e-111">**rgIds**</span><span class="sxs-lookup"><span data-stu-id="a9a5e-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="a9a5e-112">Dirección de una matriz de GUID.</span><span class="sxs-lookup"><span data-stu-id="a9a5e-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="a9a5e-113">Cada miembro de la matriz contiene un identificador de salida de OPL.</span><span class="sxs-lookup"><span data-stu-id="a9a5e-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9a5e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9a5e-114">Remarks</span></span>

<span data-ttu-id="a9a5e-115">Esta estructura se usa como un miembro de las estructuras de la copia de DRM de la copia de los OPL y del OPL de la [**reproducción de DRM \_ \_**](drmdrm-play-opl.md) para identificar grupos de identificadores de salida. [**\_ \_**](drmdrm-copy-opl.md)</span><span class="sxs-lookup"><span data-stu-id="a9a5e-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a5e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9a5e-116">Requirements</span></span>



| <span data-ttu-id="a9a5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a5e-117">Requirement</span></span> | <span data-ttu-id="a9a5e-118">Value</span><span class="sxs-lookup"><span data-stu-id="a9a5e-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a5e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9a5e-119">Header</span></span><br/> | <dl> <span data-ttu-id="a9a5e-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9a5e-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a5e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9a5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a5e-122">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="a9a5e-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





