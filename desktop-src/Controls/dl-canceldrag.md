---
title: Código de notificación de DL_CANCELDRAG (commctrl. h)
description: Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón secundario del mouse o presionando la tecla ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151289"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="b95c8-104">Código de notificación de DL \_ CANCELDRAG</span><span class="sxs-lookup"><span data-stu-id="b95c8-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="b95c8-105">Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón secundario del mouse o presionando la tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="b95c8-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="b95c8-106">Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre.</span><span class="sxs-lookup"><span data-stu-id="b95c8-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="b95c8-107">Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="b95c8-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b95c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b95c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b95c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b95c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b95c8-110">Un puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el \_ código de notificación DL CANCELDRAG, el identificador del cuadro de lista de arrastre y la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="b95c8-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b95c8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b95c8-111">Return value</span></span>

<span data-ttu-id="b95c8-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b95c8-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b95c8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b95c8-113">Remarks</span></span>

<span data-ttu-id="b95c8-114">Al procesar el \_ código de notificación DL CANCELDRAG, una aplicación puede restablecer su estado interno para indicar que el arrastre no está en vigor.</span><span class="sxs-lookup"><span data-stu-id="b95c8-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b95c8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b95c8-115">Requirements</span></span>



| <span data-ttu-id="b95c8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b95c8-116">Requirement</span></span> | <span data-ttu-id="b95c8-117">Value</span><span class="sxs-lookup"><span data-stu-id="b95c8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b95c8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b95c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b95c8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b95c8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b95c8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b95c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b95c8-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b95c8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b95c8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b95c8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b95c8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b95c8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





