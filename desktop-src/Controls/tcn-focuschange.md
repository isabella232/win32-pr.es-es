---
title: Código de notificación de TCN_FOCUSCHANGE (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el foco del botón ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- TCN_FOCUSCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801051"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="8c01a-105">Código de notificación de FOCUSCHANGE de TCN \_</span><span class="sxs-lookup"><span data-stu-id="8c01a-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="8c01a-106">Notifica a la ventana primaria de un control de pestaña que el foco del botón ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8c01a-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="8c01a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8c01a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8c01a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c01a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c01a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c01a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c01a-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="8c01a-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c01a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c01a-111">Return value</span></span>

<span data-ttu-id="8c01a-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c01a-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c01a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c01a-113">Requirements</span></span>



| <span data-ttu-id="8c01a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c01a-114">Requirement</span></span> | <span data-ttu-id="8c01a-115">Value</span><span class="sxs-lookup"><span data-stu-id="8c01a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c01a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c01a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c01a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c01a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c01a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c01a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c01a-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c01a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c01a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c01a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c01a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c01a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





