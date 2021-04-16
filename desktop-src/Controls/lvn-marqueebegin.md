---
title: Código de notificación de LVN_MARQUEEBEGIN (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que ha empezado una selección de cuadro de límite (marquesina). Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658416"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="40784-105">Código de notificación de MARQUEEBEGIN de LVN \_</span><span class="sxs-lookup"><span data-stu-id="40784-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="40784-106">Notifica a la ventana primaria de un control de vista de lista que ha empezado una selección de cuadro de límite (marquesina).</span><span class="sxs-lookup"><span data-stu-id="40784-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="40784-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="40784-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="40784-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40784-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40784-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40784-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40784-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="40784-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40784-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40784-111">Return value</span></span>

<span data-ttu-id="40784-112">Para aceptar el código de notificación, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="40784-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="40784-113">Para salir de la selección del cuadro de límite, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="40784-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="40784-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40784-114">Remarks</span></span>

<span data-ttu-id="40784-115">Una *selección de cuadro de límite* es el proceso de hacer clic en el área cliente de la ventana de vista de lista y arrastrar para seleccionar varios elementos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="40784-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="40784-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40784-116">Requirements</span></span>



| <span data-ttu-id="40784-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="40784-117">Requirement</span></span> | <span data-ttu-id="40784-118">Value</span><span class="sxs-lookup"><span data-stu-id="40784-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40784-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40784-119">Minimum supported client</span></span><br/> | <span data-ttu-id="40784-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40784-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40784-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40784-121">Minimum supported server</span></span><br/> | <span data-ttu-id="40784-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="40784-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40784-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40784-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="40784-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40784-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





