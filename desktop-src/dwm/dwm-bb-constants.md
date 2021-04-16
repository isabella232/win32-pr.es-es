---
title: Desenfoque de DWM en las constantes (dwmapi. h)
description: Marcas usadas por la \_ estructura BLURBEHIND de DWM para indicar cuál de sus miembros contiene información válida.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534516"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="9e99d-103">Desenfoque de DWM detrás de constantes</span><span class="sxs-lookup"><span data-stu-id="9e99d-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="9e99d-104">Marcas usadas por la [**estructura \_ BLURBEHIND de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar cuál de sus miembros contiene información válida.</span><span class="sxs-lookup"><span data-stu-id="9e99d-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="9e99d-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="9e99d-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e99d-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9e99d-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="9e99d-107">Se ha especificado un valor para el miembro **fEnable** .</span><span class="sxs-lookup"><span data-stu-id="9e99d-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e99d-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**</span><span class="sxs-lookup"><span data-stu-id="9e99d-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e99d-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9e99d-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="9e99d-110">Se ha especificado un valor para el miembro **hRgnBlur** .</span><span class="sxs-lookup"><span data-stu-id="9e99d-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e99d-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**</span><span class="sxs-lookup"><span data-stu-id="9e99d-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e99d-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9e99d-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="9e99d-113">Se ha especificado un valor para el miembro **fTransitionOnMaximized** .</span><span class="sxs-lookup"><span data-stu-id="9e99d-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e99d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e99d-114">Requirements</span></span>



| <span data-ttu-id="9e99d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e99d-115">Requirement</span></span> | <span data-ttu-id="9e99d-116">Value</span><span class="sxs-lookup"><span data-stu-id="9e99d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9e99d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e99d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e99d-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e99d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9e99d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e99d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e99d-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e99d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9e99d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e99d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e99d-122"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e99d-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





