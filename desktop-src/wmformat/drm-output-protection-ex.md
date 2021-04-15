---
title: DRM_OUTPUT_PROTECTION_EX estructura (wmdrmsdk. h)
description: La estructura de protección de salida de DRM \_ \_ \_ contiene información sobre una tecnología de protección de la salida. Esta estructura extiende la \_ \_ protección de salida de DRM agregando un número de versión.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709221"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="9ffa3-106">\_Estructura de \_ protección de salida de DRM \_</span><span class="sxs-lookup"><span data-stu-id="9ffa3-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="9ffa3-107">La estructura de protección de salida de DRM contiene información sobre una tecnología de protección de la salida. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ffa3-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="9ffa3-108">Esta estructura extiende **la \_ \_ protección de salida de DRM** agregando un número de versión.</span><span class="sxs-lookup"><span data-stu-id="9ffa3-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffa3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ffa3-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="9ffa3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ffa3-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ffa3-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="9ffa3-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9ffa3-112">Número de versión.</span><span class="sxs-lookup"><span data-stu-id="9ffa3-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="9ffa3-113">**guidId**</span><span class="sxs-lookup"><span data-stu-id="9ffa3-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="9ffa3-114">GUID que identifica la tecnología de protección de la salida.</span><span class="sxs-lookup"><span data-stu-id="9ffa3-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="9ffa3-115">**dwConfigData**</span><span class="sxs-lookup"><span data-stu-id="9ffa3-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="9ffa3-116">Datos de configuración de la tecnología.</span><span class="sxs-lookup"><span data-stu-id="9ffa3-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ffa3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ffa3-117">Remarks</span></span>

<span data-ttu-id="9ffa3-118">**DRM \_ La protección de salida de AUDIO \_ \_ \_ ex** y la **protección de salida de \_ vídeo DRM \_ \_ \_ ex** se definen como **\_ \_ protección de salida DRM** en instrucciones **typedef** .</span><span class="sxs-lookup"><span data-stu-id="9ffa3-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffa3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ffa3-119">Requirements</span></span>



| <span data-ttu-id="9ffa3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ffa3-120">Requirement</span></span> | <span data-ttu-id="9ffa3-121">Value</span><span class="sxs-lookup"><span data-stu-id="9ffa3-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffa3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ffa3-122">Header</span></span><br/> | <dl> <span data-ttu-id="9ffa3-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffa3-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffa3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ffa3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffa3-125">**\_protección de salida de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="9ffa3-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="9ffa3-126">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="9ffa3-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





