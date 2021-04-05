---
title: Código de notificación de NM_RCLICK (pestaña) (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el usuario ha hace clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ef2270c0-eef3-4867-8aa3-b6ff7e1a5f0f
keywords:
- Controles de Windows de código de notificación de NM_RCLICK (pestaña)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c74249e2c2984dd11dab7c4eab8147cb572f291
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079782"
---
# <a name="nm_rclick-tab-notification-code"></a><span data-ttu-id="ac073-105">\_RCLICK código de notificación de nm (pestaña)</span><span class="sxs-lookup"><span data-stu-id="ac073-105">NM\_RCLICK (tab) notification code</span></span>

<span data-ttu-id="ac073-106">Notifica a la ventana primaria de un control de pestaña que el usuario ha hace clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="ac073-106">Notifies the parent window of a tab control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="ac073-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ac073-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ac073-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac073-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac073-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac073-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="ac073-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac073-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac073-111">Return value</span></span>

<span data-ttu-id="ac073-112">Devuelve un valor distinto de cero para no permitir el procesamiento predeterminado, o cero para permitir el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ac073-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac073-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac073-113">Requirements</span></span>



| <span data-ttu-id="ac073-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac073-114">Requirement</span></span> | <span data-ttu-id="ac073-115">Value</span><span class="sxs-lookup"><span data-stu-id="ac073-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac073-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac073-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac073-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac073-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac073-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac073-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac073-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac073-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac073-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac073-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac073-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac073-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





