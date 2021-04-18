---
title: Mensaje de SB_GETRECT (commctrl. h)
description: Recupera el rectángulo delimitador de un elemento de una ventana de estado.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491993"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="44583-104">\_Mensaje GETRECT de SB</span><span class="sxs-lookup"><span data-stu-id="44583-104">SB\_GETRECT message</span></span>

<span data-ttu-id="44583-105">Recupera el rectángulo delimitador de un elemento de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="44583-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="44583-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44583-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44583-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44583-108">Índice de base cero de la parte cuyo rectángulo delimitador se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="44583-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="44583-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44583-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44583-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="44583-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44583-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44583-111">Return value</span></span>

<span data-ttu-id="44583-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="44583-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="44583-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44583-113">Requirements</span></span>



| <span data-ttu-id="44583-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="44583-114">Requirement</span></span> | <span data-ttu-id="44583-115">Value</span><span class="sxs-lookup"><span data-stu-id="44583-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44583-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44583-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44583-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="44583-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44583-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44583-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44583-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="44583-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44583-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44583-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44583-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44583-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

