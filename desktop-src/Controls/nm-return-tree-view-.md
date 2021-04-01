---
title: Código de notificación de NM_RETURN (vista de árbol) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el control tiene el foco de entrada y que el usuario ha presionado la tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- Código de notificación de NM_RETURN (vista de árbol) controles de Windows
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
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996815"
---
# <a name="nm_return-tree-view-notification-code"></a><span data-ttu-id="43e6d-105">Código de notificación de retorno de NM \_ (vista de árbol)</span><span class="sxs-lookup"><span data-stu-id="43e6d-105">NM\_RETURN (tree view) notification code</span></span>

<span data-ttu-id="43e6d-106">Notifica a la ventana primaria de un control de vista de árbol que el control tiene el foco de entrada y que el usuario ha presionado la tecla.</span><span class="sxs-lookup"><span data-stu-id="43e6d-106">Notifies a tree-view control's parent window that the control has the input focus and that the user has pressed the key.</span></span> <span data-ttu-id="43e6d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43e6d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="43e6d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43e6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43e6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43e6d-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="43e6d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e6d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43e6d-111">Return value</span></span>

<span data-ttu-id="43e6d-112">Devuelve un valor distinto de cero para evitar el procesamiento predeterminado o cero para permitir el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="43e6d-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e6d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e6d-113">Requirements</span></span>



| <span data-ttu-id="43e6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e6d-114">Requirement</span></span> | <span data-ttu-id="43e6d-115">Value</span><span class="sxs-lookup"><span data-stu-id="43e6d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43e6d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43e6d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43e6d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43e6d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43e6d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43e6d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43e6d-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="43e6d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43e6d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43e6d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43e6d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e6d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





