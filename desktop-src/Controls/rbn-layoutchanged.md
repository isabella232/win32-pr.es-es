---
title: Código de notificación de RBN_LAYOUTCHANGED (commctrl. h)
description: Lo envía un control Rebar cuando el usuario cambia el diseño de las bandas del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- RBN_LAYOUTCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150649"
---
# <a name="rbn_layoutchanged-notification-code"></a><span data-ttu-id="83a7f-105">Código de notificación de LAYOUTCHANGED de RBN \_</span><span class="sxs-lookup"><span data-stu-id="83a7f-105">RBN\_LAYOUTCHANGED notification code</span></span>

<span data-ttu-id="83a7f-106">Lo envía un control Rebar cuando el usuario cambia el diseño de las bandas del control.</span><span class="sxs-lookup"><span data-stu-id="83a7f-106">Sent by a rebar control when the user changes the layout of the control's bands.</span></span> <span data-ttu-id="83a7f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="83a7f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="83a7f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83a7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83a7f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83a7f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83a7f-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="83a7f-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83a7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83a7f-111">Return value</span></span>

<span data-ttu-id="83a7f-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="83a7f-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83a7f-113">Requirements</span></span>



| <span data-ttu-id="83a7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="83a7f-114">Requirement</span></span> | <span data-ttu-id="83a7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="83a7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83a7f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83a7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="83a7f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83a7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83a7f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83a7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="83a7f-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83a7f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83a7f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83a7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="83a7f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83a7f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





