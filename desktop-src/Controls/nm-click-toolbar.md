---
title: Código de notificación de NM_CLICK (barra de herramientas) (commctrl. h)
description: Se envía por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Código de notificación de NM_CLICK (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905689"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="441b5-105">NM \_ código de notificación de clic (barra de herramientas)</span><span class="sxs-lookup"><span data-stu-id="441b5-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="441b5-106">Se envía por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="441b5-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="441b5-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="441b5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="441b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="441b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="441b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="441b5-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="441b5-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="441b5-111">El miembro **dwItemSpec** contiene el índice de la sección en la que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="441b5-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441b5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="441b5-112">Return value</span></span>

<span data-ttu-id="441b5-113">Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="441b5-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="441b5-114">Devuelve **false** para permitir el procesamiento predeterminado del clic.</span><span class="sxs-lookup"><span data-stu-id="441b5-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="441b5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="441b5-115">Remarks</span></span>

<span data-ttu-id="441b5-116">Al hacer clic en un elemento con el botón primario del mouse, la barra de herramientas envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el código de notificación en el que se [ \_ hizo clic BN](bn-clicked.md) a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="441b5-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="441b5-117">La notificación de clic de NM \_ se envía después del mensaje de **\_ comando de WM** .</span><span class="sxs-lookup"><span data-stu-id="441b5-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="441b5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="441b5-118">Requirements</span></span>



| <span data-ttu-id="441b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="441b5-119">Requirement</span></span> | <span data-ttu-id="441b5-120">Value</span><span class="sxs-lookup"><span data-stu-id="441b5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="441b5-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="441b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="441b5-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="441b5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="441b5-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="441b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="441b5-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="441b5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="441b5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="441b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="441b5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="441b5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

