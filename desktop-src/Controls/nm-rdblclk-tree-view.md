---
title: Código de notificación de NM_RDBLCLK (vista de árbol) (commctrl. h)
description: Notifica al elemento primario de un control de vista de árbol que el usuario ha doble clic con el botón secundario del mouse en el control. Esta notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- Código de notificación de NM_RDBLCLK (vista de árbol) controles de Windows
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
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150820"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a><span data-ttu-id="f473e-105">NM \_ RDBLCLK (vista de árbol) código de notificación</span><span class="sxs-lookup"><span data-stu-id="f473e-105">NM\_RDBLCLK (tree view) notification code</span></span>

<span data-ttu-id="f473e-106">Notifica al elemento primario de un control de vista de árbol que el usuario ha doble clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="f473e-106">Notifies the parent of a tree-view control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="f473e-107">Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f473e-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f473e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f473e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f473e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f473e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f473e-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="f473e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f473e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f473e-111">Return value</span></span>

<span data-ttu-id="f473e-112">Devuelve un valor distinto de cero para evitar el procesamiento predeterminado o cero para permitir el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f473e-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f473e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f473e-113">Requirements</span></span>



| <span data-ttu-id="f473e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f473e-114">Requirement</span></span> | <span data-ttu-id="f473e-115">Value</span><span class="sxs-lookup"><span data-stu-id="f473e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f473e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f473e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f473e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f473e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f473e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f473e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f473e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f473e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f473e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f473e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f473e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f473e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





