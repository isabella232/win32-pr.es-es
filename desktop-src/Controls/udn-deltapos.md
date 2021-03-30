---
title: Código de notificación de UDN_DELTAPOS (commctrl. h)
description: Lo envía el sistema operativo a la ventana primaria de un control de flechas cuando la posición del control está a punto de cambiar.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802413"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="29748-104">Código de notificación de DELTAPOS de UDN \_</span><span class="sxs-lookup"><span data-stu-id="29748-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="29748-105">Lo envía el sistema operativo a la ventana primaria de un control de flechas cuando la posición del control está a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="29748-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="29748-106">Esto sucede cuando el usuario solicita un cambio en el valor presionando la flecha arriba o abajo del control.</span><span class="sxs-lookup"><span data-stu-id="29748-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="29748-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="29748-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="29748-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29748-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29748-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29748-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29748-110">Puntero a una estructura [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) que contiene información sobre el cambio de posición.</span><span class="sxs-lookup"><span data-stu-id="29748-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="29748-111">El miembro **IPOS** de esta estructura contiene la posición actual del control.</span><span class="sxs-lookup"><span data-stu-id="29748-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="29748-112">El miembro **iDelta** de la estructura es un entero con signo que contiene el cambio propuesto en la posición.</span><span class="sxs-lookup"><span data-stu-id="29748-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="29748-113">Si el usuario hizo clic en el botón subir, se trata de un valor positivo.</span><span class="sxs-lookup"><span data-stu-id="29748-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="29748-114">Si el usuario hizo clic en el botón abajo, se trata de un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="29748-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29748-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29748-115">Return value</span></span>

<span data-ttu-id="29748-116">Devuelve un valor distinto de cero para evitar el cambio en la posición del control o cero para permitir el cambio.</span><span class="sxs-lookup"><span data-stu-id="29748-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="29748-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29748-117">Remarks</span></span>

<span data-ttu-id="29748-118">El \_ código de notificación DELTAPOS de UDN se envía antes del mensaje [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL**](wm-hscroll.md) , que realmente cambia la posición del control.</span><span class="sxs-lookup"><span data-stu-id="29748-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="29748-119">Esto le permite examinar, permitir, modificar o denegar el cambio.</span><span class="sxs-lookup"><span data-stu-id="29748-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="29748-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29748-120">Requirements</span></span>



| <span data-ttu-id="29748-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="29748-121">Requirement</span></span> | <span data-ttu-id="29748-122">Value</span><span class="sxs-lookup"><span data-stu-id="29748-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29748-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29748-123">Minimum supported client</span></span><br/> | <span data-ttu-id="29748-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="29748-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29748-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29748-125">Minimum supported server</span></span><br/> | <span data-ttu-id="29748-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="29748-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29748-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29748-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="29748-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="29748-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29748-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="29748-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29748-130">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="29748-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

