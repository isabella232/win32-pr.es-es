---
title: Código de notificación de HDN_ITEMCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado han cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- HDN_ITEMCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078944"
---
# <a name="hdn_itemchanged-notification-code"></a><span data-ttu-id="976ca-105">Código de notificación de HDN \_ ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="976ca-105">HDN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="976ca-106">Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado han cambiado.</span><span class="sxs-lookup"><span data-stu-id="976ca-106">Notifies a header control's parent window that the attributes of a header item have changed.</span></span> <span data-ttu-id="976ca-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="976ca-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="976ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="976ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="976ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="976ca-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado, incluidos los atributos que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="976ca-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control, including the attributes that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976ca-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="976ca-111">Return value</span></span>

<span data-ttu-id="976ca-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="976ca-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="976ca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="976ca-113">Requirements</span></span>



| <span data-ttu-id="976ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="976ca-114">Requirement</span></span> | <span data-ttu-id="976ca-115">Value</span><span class="sxs-lookup"><span data-stu-id="976ca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="976ca-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="976ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="976ca-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="976ca-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="976ca-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="976ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="976ca-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="976ca-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="976ca-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="976ca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="976ca-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="976ca-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="976ca-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="976ca-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="976ca-123">**HDN \_ ITEMCHANGEDW** (Unicode) y **HDN \_ ITEMCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="976ca-123">**HDN\_ITEMCHANGEDW** (Unicode) and **HDN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



 

 





