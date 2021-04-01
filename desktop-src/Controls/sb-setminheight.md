---
title: Mensaje de SB_SETMINHEIGHT (commctrl. h)
description: Establece el alto mínimo del área de dibujo de una ventana de estado.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996809"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="8f48c-104">\_Mensaje SETMINHEIGHT de SB</span><span class="sxs-lookup"><span data-stu-id="8f48c-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="8f48c-105">Establece el alto mínimo del área de dibujo de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="8f48c-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f48c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f48c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f48c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f48c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f48c-108">Alto mínimo, en píxeles, de la ventana.</span><span class="sxs-lookup"><span data-stu-id="8f48c-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="8f48c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f48c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8f48c-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8f48c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f48c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f48c-111">Return value</span></span>

<span data-ttu-id="8f48c-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8f48c-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f48c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f48c-113">Remarks</span></span>

<span data-ttu-id="8f48c-114">El alto mínimo es la suma de *wParam* y el doble de ancho, en píxeles, del borde vertical de la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="8f48c-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="8f48c-115">Una aplicación debe enviar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) a la ventana de estado para volver a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="8f48c-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="8f48c-116">Los parámetros *wParam* e *lParam* del mensaje **de \_ tamaño de WM** deben establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="8f48c-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f48c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f48c-117">Requirements</span></span>



| <span data-ttu-id="8f48c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f48c-118">Requirement</span></span> | <span data-ttu-id="8f48c-119">Value</span><span class="sxs-lookup"><span data-stu-id="8f48c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f48c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f48c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f48c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f48c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f48c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f48c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f48c-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f48c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f48c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f48c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f48c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f48c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

