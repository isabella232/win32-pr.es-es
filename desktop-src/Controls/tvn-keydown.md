---
title: Código de notificación de TVN_KEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el usuario presionó una tecla y el control de vista de árbol tiene el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489016"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="6ed34-105">\_Código de notificación KEYDOWN de TVN</span><span class="sxs-lookup"><span data-stu-id="6ed34-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="6ed34-106">Notifica a la ventana primaria de un control de vista de árbol que el usuario presionó una tecla y el control de vista de árbol tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="6ed34-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="6ed34-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed34-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="6ed34-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ed34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ed34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ed34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ed34-110">Puntero a una estructura [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="6ed34-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="6ed34-111">El miembro **wVKey** especifica el código de la clave virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed34-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ed34-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ed34-112">Return value</span></span>

<span data-ttu-id="6ed34-113">Si el miembro **wVKey** de *lParam* es un código de tecla de carácter, el carácter se usará como parte de una búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="6ed34-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="6ed34-114">Devuelve un valor distinto de cero para excluir el carácter de la búsqueda incremental o cero para incluir el carácter en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6ed34-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="6ed34-115">Para todas las demás claves, se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="6ed34-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed34-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed34-116">Requirements</span></span>



| <span data-ttu-id="6ed34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed34-117">Requirement</span></span> | <span data-ttu-id="6ed34-118">Value</span><span class="sxs-lookup"><span data-stu-id="6ed34-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed34-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ed34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed34-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ed34-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ed34-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ed34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed34-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ed34-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ed34-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ed34-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed34-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed34-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





