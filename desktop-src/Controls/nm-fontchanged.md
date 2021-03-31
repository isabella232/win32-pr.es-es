---
title: Código de notificación de NM_FONTCHANGED (commctrl. h)
description: Lo envía un control de vista de lista cuando el control ha cambiado una fuente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904997"
---
# <a name="nm_fontchanged-notification-code"></a><span data-ttu-id="f934e-105">Código de notificación de NM \_ FONTCHANGED</span><span class="sxs-lookup"><span data-stu-id="f934e-105">NM\_FONTCHANGED notification code</span></span>

<span data-ttu-id="f934e-106">Lo envía un control de vista de lista cuando el control ha cambiado una fuente.</span><span class="sxs-lookup"><span data-stu-id="f934e-106">Sent by a list-view control when the control has changed a font.</span></span> <span data-ttu-id="f934e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f934e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f934e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f934e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f934e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f934e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f934e-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="f934e-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f934e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f934e-111">Return value</span></span>

<span data-ttu-id="f934e-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f934e-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f934e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f934e-113">Requirements</span></span>



| <span data-ttu-id="f934e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f934e-114">Requirement</span></span> | <span data-ttu-id="f934e-115">Value</span><span class="sxs-lookup"><span data-stu-id="f934e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f934e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f934e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f934e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f934e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f934e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f934e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f934e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f934e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f934e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f934e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f934e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f934e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





