---
title: DRM_OUTPUT_PROTECTION estructura (wmdrmsdk. h)
description: La estructura de protección de salida de DRM \_ \_ contiene información sobre una tecnología de protección de la salida.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708947"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="5a93d-105">Estructura de protección de \_ salida de DRM \_</span><span class="sxs-lookup"><span data-stu-id="5a93d-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="5a93d-106">La estructura de **\_ \_ protección de salida de DRM** contiene información sobre una tecnología de protección de la salida.</span><span class="sxs-lookup"><span data-stu-id="5a93d-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a93d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a93d-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="5a93d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a93d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a93d-109">**guidId**</span><span class="sxs-lookup"><span data-stu-id="5a93d-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="5a93d-110">GUID que identifica la tecnología de protección de la salida.</span><span class="sxs-lookup"><span data-stu-id="5a93d-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="5a93d-111">**bConfigData**</span><span class="sxs-lookup"><span data-stu-id="5a93d-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="5a93d-112">Datos de configuración de la tecnología.</span><span class="sxs-lookup"><span data-stu-id="5a93d-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a93d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a93d-113">Remarks</span></span>

<span data-ttu-id="5a93d-114">**DRM \_ La \_ \_** protección de salida de audio y la **protección de \_ \_ salida \_ de vídeo DRM** se definen como **\_ \_ protección de salida DRM** en instrucciones **typedef** .</span><span class="sxs-lookup"><span data-stu-id="5a93d-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a93d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a93d-115">Requirements</span></span>



| <span data-ttu-id="5a93d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a93d-116">Requirement</span></span> | <span data-ttu-id="5a93d-117">Value</span><span class="sxs-lookup"><span data-stu-id="5a93d-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a93d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a93d-118">Header</span></span><br/> | <dl> <span data-ttu-id="5a93d-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a93d-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a93d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a93d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a93d-121">**\_protección de salida DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="5a93d-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="5a93d-122">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="5a93d-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





