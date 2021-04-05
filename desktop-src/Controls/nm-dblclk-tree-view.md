---
title: Código de notificación de NM_DBLCLK (vista de árbol) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el usuario ha hace doble clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- Código de notificación de NM_DBLCLK (vista de árbol) controles de Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078860"
---
# <a name="nm_dblclk-tree-view-notification-code"></a><span data-ttu-id="45c13-105">NM \_ DBLCLK (vista de árbol) código de notificación</span><span class="sxs-lookup"><span data-stu-id="45c13-105">NM\_DBLCLK (tree view) notification code</span></span>

<span data-ttu-id="45c13-106">Notifica a la ventana primaria de un control de vista de árbol que el usuario ha hace doble clic en el botón primario del mouse dentro del control.</span><span class="sxs-lookup"><span data-stu-id="45c13-106">Notifies the parent window of a tree-view control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="45c13-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="45c13-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="45c13-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45c13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45c13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45c13-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="45c13-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c13-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45c13-111">Return value</span></span>

<span data-ttu-id="45c13-112">Devuelve un valor distinto de cero para evitar el procesamiento predeterminado o cero para permitir el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="45c13-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c13-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c13-113">Requirements</span></span>



| <span data-ttu-id="45c13-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c13-114">Requirement</span></span> | <span data-ttu-id="45c13-115">Value</span><span class="sxs-lookup"><span data-stu-id="45c13-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45c13-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45c13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="45c13-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45c13-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45c13-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45c13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="45c13-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45c13-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45c13-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45c13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c13-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c13-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





