---
title: Código de notificación de NM_DBLCLK (pestaña) (commctrl. h)
description: Notifica a una ventana primaria de un control de pestaña que el usuario ha hace doble clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Controles de Windows de código de notificación de NM_DBLCLK (pestaña)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150877"
---
# <a name="nm_dblclk-tab-notification-code"></a><span data-ttu-id="39e09-105">\_DBLCLK código de notificación de nm (pestaña)</span><span class="sxs-lookup"><span data-stu-id="39e09-105">NM\_DBLCLK (tab) notification code</span></span>

<span data-ttu-id="39e09-106">Notifica a una ventana primaria de un control de pestaña que el usuario ha hace doble clic en el botón primario del mouse dentro del control.</span><span class="sxs-lookup"><span data-stu-id="39e09-106">Notifies a parent window of a tab control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="39e09-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="39e09-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="39e09-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39e09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e09-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39e09-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39e09-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="39e09-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e09-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39e09-111">Return value</span></span>

<span data-ttu-id="39e09-112">Devuelve un valor distinto de cero para no permitir el procesamiento predeterminado, o cero para permitir el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="39e09-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e09-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39e09-113">Requirements</span></span>



| <span data-ttu-id="39e09-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e09-114">Requirement</span></span> | <span data-ttu-id="39e09-115">Value</span><span class="sxs-lookup"><span data-stu-id="39e09-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39e09-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39e09-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39e09-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39e09-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39e09-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39e09-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39e09-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="39e09-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39e09-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39e09-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39e09-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e09-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





