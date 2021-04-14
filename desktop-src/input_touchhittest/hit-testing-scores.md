---
title: Puntuaciones de la prueba de posicionamiento táctil
description: Las constantes siguientes identifican las puntuaciones de pruebas de posicionamiento posibles para un objeto, con respecto a otros objetos que forman una intersección con el área de contacto táctil.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534005"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="120b2-103">Puntuaciones de la prueba de posicionamiento táctil</span><span class="sxs-lookup"><span data-stu-id="120b2-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="120b2-104">Las constantes siguientes identifican las puntuaciones de pruebas de posicionamiento posibles para un objeto, con respecto a otros objetos que forman una intersección con el área de contacto táctil.</span><span class="sxs-lookup"><span data-stu-id="120b2-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="120b2-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="120b2-105">Constant/value</span></span> | <span data-ttu-id="120b2-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="120b2-106">Description</span></span> |
|---|---|
| <span data-ttu-id="120b2-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0X0</span><span class="sxs-lookup"><span data-stu-id="120b2-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="120b2-108">El objeto es el destino más probable.</span><span class="sxs-lookup"><span data-stu-id="120b2-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="120b2-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span><span class="sxs-lookup"><span data-stu-id="120b2-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="120b2-110">El objeto es el destino menos probable.</span><span class="sxs-lookup"><span data-stu-id="120b2-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="120b2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="120b2-111">Requirements</span></span>

| <span data-ttu-id="120b2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="120b2-112">Requirement</span></span> | <span data-ttu-id="120b2-113">Value</span><span class="sxs-lookup"><span data-stu-id="120b2-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="120b2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="120b2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="120b2-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="120b2-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="120b2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="120b2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="120b2-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="120b2-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="120b2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="120b2-118">Header</span></span><br/>                   | <span data-ttu-id="120b2-119">Winuser. h</span><span class="sxs-lookup"><span data-stu-id="120b2-119">Winuser.h</span></span> |
