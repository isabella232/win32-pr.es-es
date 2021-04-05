---
title: Código de notificación de NM_RDBLCLK (pestaña) (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el usuario ha doble clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- Controles de Windows de código de notificación de NM_RDBLCLK (pestaña)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078855"
---
# <a name="nm_rdblclk-tab-notification-code"></a><span data-ttu-id="e6a39-105">\_RDBLCLK código de notificación de nm (pestaña)</span><span class="sxs-lookup"><span data-stu-id="e6a39-105">NM\_RDBLCLK (tab) notification code</span></span>

<span data-ttu-id="e6a39-106">Notifica a la ventana primaria de un control de pestaña que el usuario ha doble clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="e6a39-106">Notifies the parent window of a tab control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="e6a39-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a39-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e6a39-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6a39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a39-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6a39-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a39-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="e6a39-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a39-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6a39-111">Return value</span></span>

<span data-ttu-id="e6a39-112">Devuelve un valor distinto de cero para no permitir el procesamiento predeterminado, o cero para permitir el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e6a39-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a39-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6a39-113">Requirements</span></span>



| <span data-ttu-id="e6a39-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a39-114">Requirement</span></span> | <span data-ttu-id="e6a39-115">Value</span><span class="sxs-lookup"><span data-stu-id="e6a39-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a39-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6a39-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a39-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a39-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6a39-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6a39-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a39-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a39-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6a39-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6a39-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a39-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a39-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





