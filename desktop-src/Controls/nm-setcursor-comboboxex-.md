---
title: Código de notificación de NM_SETCURSOR (ComboBoxEx) (commctrl. h)
description: Notifica a la ventana primaria de un control ComboBoxEx que el control está estableciendo el cursor en respuesta a un \_ mensaje de SETCURSOR de WM. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- Controles de Windows de código de notificación de NM_SETCURSOR (ComboBoxEx)
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803151"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a><span data-ttu-id="bf067-105">Código de notificación de NM \_ SETCURSOR (ComboBoxEx)</span><span class="sxs-lookup"><span data-stu-id="bf067-105">NM\_SETCURSOR (ComboBoxEx) notification code</span></span>

<span data-ttu-id="bf067-106">Notifica a la ventana primaria de un control ComboBoxEx que el control está estableciendo el cursor en respuesta a un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="bf067-106">Notifies a ComboBoxEx control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="bf067-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bf067-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bf067-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf067-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf067-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf067-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf067-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="bf067-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf067-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf067-111">Return value</span></span>

<span data-ttu-id="bf067-112">Devuelve cero para permitir que el control establezca el cursor o un valor distinto de cero para evitar que el control establezca el cursor.</span><span class="sxs-lookup"><span data-stu-id="bf067-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf067-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf067-113">Requirements</span></span>



| <span data-ttu-id="bf067-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf067-114">Requirement</span></span> | <span data-ttu-id="bf067-115">Value</span><span class="sxs-lookup"><span data-stu-id="bf067-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf067-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf067-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf067-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bf067-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf067-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf067-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf067-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf067-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf067-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf067-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf067-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf067-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

