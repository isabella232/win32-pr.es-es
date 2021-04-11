---
title: Código de notificación de HDN_DIVIDERDBLCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el área de división del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079784"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="f0e52-105">Código de notificación de DIVIDERDBLCLICK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="f0e52-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="f0e52-106">Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el área de división del control.</span><span class="sxs-lookup"><span data-stu-id="f0e52-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="f0e52-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e52-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f0e52-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0e52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e52-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0e52-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e52-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se hizo doble clic.</span><span class="sxs-lookup"><span data-stu-id="f0e52-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e52-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0e52-111">Return value</span></span>

<span data-ttu-id="f0e52-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f0e52-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e52-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0e52-113">Requirements</span></span>



| <span data-ttu-id="f0e52-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0e52-114">Requirement</span></span> | <span data-ttu-id="f0e52-115">Value</span><span class="sxs-lookup"><span data-stu-id="f0e52-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e52-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0e52-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e52-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0e52-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0e52-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0e52-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e52-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0e52-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0e52-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0e52-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e52-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e52-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f0e52-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f0e52-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f0e52-123">**HDN \_ DIVIDERDBLCLICKW** (Unicode) y **HDN \_ DIVIDERDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f0e52-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 





