---
title: Código de notificación de NM_RETURN (vista de lista) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que el control tiene el foco de entrada y que el usuario ha presionado la tecla entrar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- NM_RETURN (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996816"
---
# <a name="nm_return-list-view-notification-code"></a><span data-ttu-id="c8c80-105">Código de notificación de retorno de NM \_ (vista de lista)</span><span class="sxs-lookup"><span data-stu-id="c8c80-105">NM\_RETURN (list view) notification code</span></span>

<span data-ttu-id="c8c80-106">Notifica a la ventana primaria de un control de vista de lista que el control tiene el foco de entrada y que el usuario ha presionado la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="c8c80-106">Notifies a list-view control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="c8c80-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8c80-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c8c80-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8c80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c80-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8c80-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8c80-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c8c80-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c80-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8c80-111">Return value</span></span>

<span data-ttu-id="c8c80-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c8c80-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c80-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c80-113">Requirements</span></span>



| <span data-ttu-id="c8c80-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c80-114">Requirement</span></span> | <span data-ttu-id="c8c80-115">Value</span><span class="sxs-lookup"><span data-stu-id="c8c80-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c80-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c80-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c8c80-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8c80-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c80-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8c80-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8c80-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8c80-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8c80-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c80-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





