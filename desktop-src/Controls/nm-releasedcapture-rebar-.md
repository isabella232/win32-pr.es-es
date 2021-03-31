---
title: Código de notificación de NM_RELEASEDCAPTURE (rebar) (commctrl. h)
description: Notifica a la ventana primaria de un control rebar que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- Código de notificación NM_RELEASEDCAPTURE (rebar) controles de Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f5367a0a5d5fac0948493ef70e4be1140013c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996461"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a><span data-ttu-id="90335-105">Código de notificación de NM \_ RELEASEDCAPTURE (rebar)</span><span class="sxs-lookup"><span data-stu-id="90335-105">NM\_RELEASEDCAPTURE (rebar) notification code</span></span>

<span data-ttu-id="90335-106">Notifica a la ventana primaria de un control rebar que el control está liberando la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="90335-106">Notifies a rebar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="90335-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90335-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="90335-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90335-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90335-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90335-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90335-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="90335-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90335-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90335-111">Return value</span></span>

<span data-ttu-id="90335-112">El control omite el valor devuelto de este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="90335-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="90335-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90335-113">Requirements</span></span>



| <span data-ttu-id="90335-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="90335-114">Requirement</span></span> | <span data-ttu-id="90335-115">Value</span><span class="sxs-lookup"><span data-stu-id="90335-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90335-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90335-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90335-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="90335-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90335-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90335-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90335-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="90335-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90335-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90335-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90335-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90335-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





