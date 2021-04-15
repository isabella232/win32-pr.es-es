---
title: DRM_COPY_OPL estructura (wmdrmsdk. h)
description: La estructura de copia del OPL de DRM \_ \_ contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de copia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709044"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="201b8-105">Estructura del OPL de \_ copia de DRM \_</span><span class="sxs-lookup"><span data-stu-id="201b8-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="201b8-106">La estructura de **\_ copia del \_ OPL de DRM** contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de copia.</span><span class="sxs-lookup"><span data-stu-id="201b8-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="201b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="201b8-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="201b8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="201b8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="201b8-109">**wMinimumCopyLevel**</span><span class="sxs-lookup"><span data-stu-id="201b8-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="201b8-110">Mínimo de OPL para las acciones de copia.</span><span class="sxs-lookup"><span data-stu-id="201b8-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="201b8-111">**oplIdIncludes**</span><span class="sxs-lookup"><span data-stu-id="201b8-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="201b8-112">[**DRM \_ OPL la estructura de los \_ \_ identificadores de salida**](drmdrm-opl-output-ids.md) que contiene los identificadores de las tecnologías que se van a permitir.</span><span class="sxs-lookup"><span data-stu-id="201b8-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="201b8-113">Este miembro se usa para las tecnologías de salida que tienen asignado OPLs inferior al nivel mínimo de copia, pero en el que se puede copiar el contenido.</span><span class="sxs-lookup"><span data-stu-id="201b8-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="201b8-114">**oplIdExcludes**</span><span class="sxs-lookup"><span data-stu-id="201b8-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="201b8-115">[**DRM \_ OPL \_ \_**](drmdrm-opl-output-ids.md) la estructura de IDS de salida que contiene los identificadores de salida de tecnologías que se van a restringir.</span><span class="sxs-lookup"><span data-stu-id="201b8-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="201b8-116">Este miembro se usa para las tecnologías de salida asignadas a OPLs que superan el nivel mínimo de copia, pero que el emisor de la licencia no concede derechos de copia en.</span><span class="sxs-lookup"><span data-stu-id="201b8-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="201b8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="201b8-117">Requirements</span></span>



| <span data-ttu-id="201b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="201b8-118">Requirement</span></span> | <span data-ttu-id="201b8-119">Value</span><span class="sxs-lookup"><span data-stu-id="201b8-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="201b8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="201b8-120">Header</span></span><br/> | <dl> <span data-ttu-id="201b8-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="201b8-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="201b8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="201b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201b8-123">**el \_ OPL de reproducción de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="201b8-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="201b8-124">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="201b8-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





