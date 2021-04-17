---
title: Código de notificación de BCN_DROPDOWN (Winuser. h)
description: Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de mensaje de notificación de WM \_ .
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656517"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="f933e-105">\_Código de notificación de desplegable BCN</span><span class="sxs-lookup"><span data-stu-id="f933e-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="f933e-106">Se envía cuando el usuario hace clic en una flecha desplegable de un botón.</span><span class="sxs-lookup"><span data-stu-id="f933e-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="f933e-107">La ventana primaria del control recibe este código de notificación en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f933e-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f933e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f933e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f933e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f933e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f933e-110">Puntero a una estructura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="f933e-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="f933e-111">El miembro **rcButton** se establece para describir el área desplegable.</span><span class="sxs-lookup"><span data-stu-id="f933e-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f933e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f933e-112">Return value</span></span>

<span data-ttu-id="f933e-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f933e-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f933e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f933e-114">Remarks</span></span>

<span data-ttu-id="f933e-115">El receptor de notificaciones convierte **lParam** para recuperar la estructura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="f933e-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="f933e-116">**WParam** contiene el identificador del control que envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f933e-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="f933e-117">El control de botón debe tener un estilo de botón de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="f933e-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f933e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f933e-118">Requirements</span></span>



| <span data-ttu-id="f933e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f933e-119">Requirement</span></span> | <span data-ttu-id="f933e-120">Value</span><span class="sxs-lookup"><span data-stu-id="f933e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f933e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f933e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f933e-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f933e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f933e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f933e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f933e-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f933e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f933e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f933e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f933e-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f933e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





