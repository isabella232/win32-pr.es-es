---
title: Código de notificación de NM_THEMECHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control que el tema ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079564"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="ef74c-105">Código de notificación de NM \_ THEMECHANGED</span><span class="sxs-lookup"><span data-stu-id="ef74c-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="ef74c-106">Notifica a la ventana primaria de un control que el tema ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ef74c-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="ef74c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ef74c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ef74c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef74c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef74c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef74c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef74c-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="ef74c-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef74c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef74c-111">Return value</span></span>

<span data-ttu-id="ef74c-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ef74c-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef74c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef74c-113">Requirements</span></span>



| <span data-ttu-id="ef74c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef74c-114">Requirement</span></span> | <span data-ttu-id="ef74c-115">Value</span><span class="sxs-lookup"><span data-stu-id="ef74c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef74c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef74c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef74c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef74c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef74c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef74c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef74c-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef74c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef74c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef74c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef74c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef74c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





