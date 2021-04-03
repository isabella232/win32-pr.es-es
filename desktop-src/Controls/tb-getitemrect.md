---
title: Mensaje de TB_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador de un botón de una barra de herramientas.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905453"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="1497f-104">\_Mensaje GETITEMRECT TB</span><span class="sxs-lookup"><span data-stu-id="1497f-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="1497f-105">Recupera el rectángulo delimitador de un botón de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1497f-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1497f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1497f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1497f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1497f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1497f-108">Índice de base cero del botón para el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="1497f-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="1497f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1497f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1497f-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe las coordenadas de cliente del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="1497f-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1497f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1497f-111">Return value</span></span>

<span data-ttu-id="1497f-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1497f-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1497f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1497f-113">Remarks</span></span>

<span data-ttu-id="1497f-114">Este mensaje no recupera el rectángulo delimitador de los botones cuyo estado está establecido en el valor [**\_ oculto TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="1497f-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1497f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1497f-115">Requirements</span></span>



| <span data-ttu-id="1497f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1497f-116">Requirement</span></span> | <span data-ttu-id="1497f-117">Value</span><span class="sxs-lookup"><span data-stu-id="1497f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1497f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1497f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1497f-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1497f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1497f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1497f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1497f-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1497f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1497f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1497f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1497f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1497f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

