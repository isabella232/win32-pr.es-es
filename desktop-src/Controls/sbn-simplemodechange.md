---
title: Código de notificación de SBN_SIMPLEMODECHANGE (commctrl. h)
description: Lo envía un control de barra de estado cuando cambia el modo simple debido a un \_ mensaje simple de SB. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658288"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="b3071-105">Código de notificación de SIMPLEMODECHANGE de SBN \_</span><span class="sxs-lookup"><span data-stu-id="b3071-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="b3071-106">Lo envía un control de barra de estado cuando cambia el modo simple debido a un mensaje [**\_ simple de SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="b3071-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="b3071-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b3071-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b3071-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3071-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3071-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3071-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3071-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="b3071-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3071-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3071-111">Return value</span></span>

<span data-ttu-id="b3071-112">El valor devuelto se omite en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="b3071-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3071-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3071-113">Requirements</span></span>



| <span data-ttu-id="b3071-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3071-114">Requirement</span></span> | <span data-ttu-id="b3071-115">Value</span><span class="sxs-lookup"><span data-stu-id="b3071-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3071-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3071-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3071-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3071-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3071-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3071-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3071-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3071-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3071-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3071-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3071-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3071-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





