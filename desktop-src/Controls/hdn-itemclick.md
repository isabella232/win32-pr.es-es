---
title: Código de notificación de HDN_ITEMCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905519"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="6b0fa-105">Código de notificación de ITEMCLICK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="6b0fa-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="6b0fa-106">Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el control.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="6b0fa-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0fa-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6b0fa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b0fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b0fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0fa-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que identifica el control de encabezado y especifica el índice del elemento de encabezado en el que se hizo clic y el botón del mouse que se usa para hacer clic en el elemento.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="6b0fa-111">El miembro **pItem** se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0fa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b0fa-112">Return value</span></span>

<span data-ttu-id="6b0fa-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0fa-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b0fa-114">Remarks</span></span>

<span data-ttu-id="6b0fa-115">Un control de encabezado envía este código de notificación cuando el usuario suelta el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0fa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b0fa-116">Requirements</span></span>



| <span data-ttu-id="6b0fa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0fa-117">Requirement</span></span> | <span data-ttu-id="6b0fa-118">Value</span><span class="sxs-lookup"><span data-stu-id="6b0fa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0fa-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b0fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0fa-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6b0fa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b0fa-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b0fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0fa-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b0fa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b0fa-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b0fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b0fa-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b0fa-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6b0fa-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6b0fa-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6b0fa-126">**HDN \_ ITEMCLICKW** (Unicode) y **HDN \_ ITEMCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





