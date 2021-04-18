---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY estructura (wmdrmsdk. h)
description: La estructura WMDRMNET de la \_ directiva \_ de TRANSCRYPTPLAY contiene la información de la Directiva para reproducir contenido con DRM de Windows Media para dispositivos de red.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649528"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="7bed3-105">\_ \_ Estructura TRANSCRYPTPLAY de la Directiva WMDRMNET</span><span class="sxs-lookup"><span data-stu-id="7bed3-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="7bed3-106">La estructura WMDRMNET de la **\_ Directiva de \_ TRANSCRYPTPLAY** contiene la información de la Directiva para reproducir contenido con DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="7bed3-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bed3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bed3-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="7bed3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7bed3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7bed3-109">**GLOBALS**</span><span class="sxs-lookup"><span data-stu-id="7bed3-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="7bed3-110">Estructura global de directivas.</span><span class="sxs-lookup"><span data-stu-id="7bed3-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="7bed3-111">**playOPLs**</span><span class="sxs-lookup"><span data-stu-id="7bed3-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="7bed3-112">Niveles de protección de salida para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7bed3-112">Output protection levels for playback.</span></span> <span data-ttu-id="7bed3-113">**WMDRMNET \_ La Directiva de \_ \_ OPL de Play** es un tipo definido como el [**OPL de reproducción de DRM \_ \_ \_**](drm-play-opl-ex.md).</span><span class="sxs-lookup"><span data-stu-id="7bed3-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bed3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bed3-114">Remarks</span></span>

<span data-ttu-id="7bed3-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7bed3-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bed3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bed3-116">Requirements</span></span>



| <span data-ttu-id="7bed3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bed3-117">Requirement</span></span> | <span data-ttu-id="7bed3-118">Value</span><span class="sxs-lookup"><span data-stu-id="7bed3-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bed3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bed3-119">Header</span></span><br/> | <dl> <span data-ttu-id="7bed3-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bed3-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bed3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bed3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bed3-122">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="7bed3-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="7bed3-123">**\_Directiva WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="7bed3-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





