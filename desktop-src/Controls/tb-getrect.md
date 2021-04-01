---
title: Mensaje de TB_GETRECT (commctrl. h)
description: Recupera el rectángulo delimitador para un botón de la barra de herramientas especificado.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- TB_GETRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905643"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="0b8a9-104">\_Mensaje GETRECT TB</span><span class="sxs-lookup"><span data-stu-id="0b8a9-104">TB\_GETRECT message</span></span>

<span data-ttu-id="0b8a9-105">Recupera el rectángulo delimitador para un botón de la barra de herramientas especificado.</span><span class="sxs-lookup"><span data-stu-id="0b8a9-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b8a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b8a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b8a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b8a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b8a9-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="0b8a9-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="0b8a9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b8a9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b8a9-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="0b8a9-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b8a9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b8a9-111">Return value</span></span>

<span data-ttu-id="0b8a9-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="0b8a9-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b8a9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b8a9-113">Remarks</span></span>

<span data-ttu-id="0b8a9-114">Este mensaje no recupera el rectángulo delimitador de los botones cuyo estado está establecido en el valor [**\_ oculto TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="0b8a9-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8a9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b8a9-115">Requirements</span></span>



| <span data-ttu-id="0b8a9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b8a9-116">Requirement</span></span> | <span data-ttu-id="0b8a9-117">Value</span><span class="sxs-lookup"><span data-stu-id="0b8a9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8a9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b8a9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b8a9-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0b8a9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b8a9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b8a9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b8a9-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b8a9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b8a9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b8a9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b8a9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b8a9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

