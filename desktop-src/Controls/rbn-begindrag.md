---
title: Código de notificación de RBN_BEGINDRAG (commctrl. h)
description: Lo envía un control Rebar cuando el usuario comienza a arrastrar una banda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- RBN_BEGINDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489232"
---
# <a name="rbn_begindrag-notification-code"></a><span data-ttu-id="10e19-105">Código de notificación de BEGINDRAG de RBN \_</span><span class="sxs-lookup"><span data-stu-id="10e19-105">RBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="10e19-106">Lo envía un control Rebar cuando el usuario comienza a arrastrar una banda.</span><span class="sxs-lookup"><span data-stu-id="10e19-106">Sent by a rebar control when the user begins dragging a band.</span></span> <span data-ttu-id="10e19-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="10e19-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="10e19-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10e19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10e19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10e19-110">Puntero a una estructura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="10e19-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e19-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10e19-111">Return value</span></span>

<span data-ttu-id="10e19-112">Devuelve cero para permitir que el rebar continúe la operación de arrastre, o un valor distinto de cero para anular la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="10e19-112">Return zero to allow the rebar to continue the drag operation, or nonzero to abort the drag operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e19-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10e19-113">Requirements</span></span>



| <span data-ttu-id="10e19-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10e19-114">Requirement</span></span> | <span data-ttu-id="10e19-115">Value</span><span class="sxs-lookup"><span data-stu-id="10e19-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10e19-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10e19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10e19-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10e19-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10e19-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10e19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10e19-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="10e19-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10e19-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10e19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e19-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10e19-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





