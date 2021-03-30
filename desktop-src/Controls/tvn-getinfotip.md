---
title: Código de notificación de TVN_GETINFOTIP (commctrl. h)
description: Enviado por un control de vista de árbol que tiene el estilo de recuadro de TV \_ . Este código de notificación se envía cuando el control solicita información de texto adicional que se va a mostrar en una información sobre herramientas. El código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802840"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="f385f-106">Código de notificación de GETINFOTIP de TVN \_</span><span class="sxs-lookup"><span data-stu-id="f385f-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="f385f-107">Enviado por un control de vista de árbol que tiene el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f385f-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="f385f-108">Este código de notificación se envía cuando el control solicita información de texto adicional que se va a mostrar en una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f385f-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="f385f-109">El código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f385f-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="f385f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f385f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f385f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f385f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f385f-112">Puntero a una estructura [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="f385f-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f385f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f385f-113">Return value</span></span>

<span data-ttu-id="f385f-114">El control omite el valor devuelto para este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="f385f-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f385f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f385f-115">Remarks</span></span>

<span data-ttu-id="f385f-116">Este código de notificación solo lo envían los controles de vista de árbol que tienen el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f385f-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f385f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f385f-117">Requirements</span></span>



| <span data-ttu-id="f385f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f385f-118">Requirement</span></span> | <span data-ttu-id="f385f-119">Value</span><span class="sxs-lookup"><span data-stu-id="f385f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f385f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f385f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f385f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f385f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f385f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f385f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f385f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f385f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f385f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f385f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f385f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f385f-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f385f-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f385f-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f385f-127">**TVN \_ GETINFOTIPW** (Unicode) y **TVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f385f-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





