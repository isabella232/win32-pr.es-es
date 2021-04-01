---
title: Código de notificación de PGN_SCROLL (commctrl. h)
description: Notifica a la ventana primaria de un control de paginación que la ventana contenida está a punto de desplazarse. Esta notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150189"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="83202-105">Código de notificación de desplazamiento de PGN \_</span><span class="sxs-lookup"><span data-stu-id="83202-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="83202-106">Notifica a la ventana primaria de un control de paginación que la ventana contenida está a punto de desplazarse.</span><span class="sxs-lookup"><span data-stu-id="83202-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="83202-107">Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="83202-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="83202-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83202-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83202-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83202-110">Puntero a una estructura [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) que contiene y recibe información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="83202-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="83202-111">El miembro **iDir** de esta estructura indica la dirección del desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="83202-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="83202-112">Los miembros **iXpos** y **iYpos** contienen la posición horizontal y vertical de la ventana contenida antes del desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="83202-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="83202-113">El miembro **iScroll** contiene la diferencia de desplazamiento predeterminada.</span><span class="sxs-lookup"><span data-stu-id="83202-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="83202-114">Si lo desea, puede modificar este miembro a una cantidad de desplazamiento diferente.</span><span class="sxs-lookup"><span data-stu-id="83202-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83202-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83202-115">Return value</span></span>

<span data-ttu-id="83202-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="83202-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="83202-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83202-117">Requirements</span></span>



| <span data-ttu-id="83202-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83202-118">Requirement</span></span> | <span data-ttu-id="83202-119">Value</span><span class="sxs-lookup"><span data-stu-id="83202-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83202-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83202-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83202-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83202-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83202-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83202-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83202-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83202-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83202-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83202-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83202-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83202-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





