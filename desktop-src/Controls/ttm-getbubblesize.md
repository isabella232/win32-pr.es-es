---
title: Mensaje de TTM_GETBUBBLESIZE (commctrl. h)
description: Devuelve el ancho y el alto de un control ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150309"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="0cee6-104">TTM \_ GETBUBBLESIZE</span><span class="sxs-lookup"><span data-stu-id="0cee6-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="0cee6-105">Devuelve el ancho y el alto de un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="0cee6-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cee6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cee6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cee6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cee6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0cee6-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0cee6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0cee6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cee6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cee6-110">Puntero a la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="0cee6-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cee6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cee6-111">Return value</span></span>

<span data-ttu-id="0cee6-112">Devuelve el ancho de la información sobre herramientas en la palabra baja y la altura de la palabra alta si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="0cee6-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="0cee6-113">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="0cee6-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cee6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cee6-114">Remarks</span></span>

<span data-ttu-id="0cee6-115">Si las \_ marcas de seguimiento y ttf de ttf \_ se establecen en el miembro **uFlags** de la estructura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , este mensaje se puede usar para ayudar a colocar la información sobre herramientas con precisión.</span><span class="sxs-lookup"><span data-stu-id="0cee6-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cee6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cee6-116">Requirements</span></span>



| <span data-ttu-id="0cee6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cee6-117">Requirement</span></span> | <span data-ttu-id="0cee6-118">Value</span><span class="sxs-lookup"><span data-stu-id="0cee6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cee6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cee6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cee6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0cee6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cee6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cee6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cee6-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cee6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cee6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cee6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cee6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cee6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





