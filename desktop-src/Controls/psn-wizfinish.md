---
title: Código de notificación de PSN_WIZFINISH (Prsht. h)
description: Notifica a una página que el usuario ha pulsado el botón Finalizar en un asistente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491783"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="d1afc-105">Código de notificación de WIZFINISH de PSN \_</span><span class="sxs-lookup"><span data-stu-id="d1afc-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="d1afc-106">Notifica a una página que el usuario ha pulsado el botón **Finalizar** en un asistente.</span><span class="sxs-lookup"><span data-stu-id="d1afc-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="d1afc-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d1afc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d1afc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1afc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1afc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1afc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1afc-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="d1afc-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="d1afc-111">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1afc-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="d1afc-112">El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.</span><span class="sxs-lookup"><span data-stu-id="d1afc-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1afc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1afc-113">Return value</span></span>

-   <span data-ttu-id="d1afc-114">Devuelve **true** para evitar que finalice el asistente.</span><span class="sxs-lookup"><span data-stu-id="d1afc-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="d1afc-115">Versión 5,80.</span><span class="sxs-lookup"><span data-stu-id="d1afc-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="d1afc-116">y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d1afc-116">and later.</span></span> <span data-ttu-id="d1afc-117">Devuelve un identificador de ventana para evitar que finalice el asistente.</span><span class="sxs-lookup"><span data-stu-id="d1afc-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="d1afc-118">El asistente establecerá el foco en esa ventana.</span><span class="sxs-lookup"><span data-stu-id="d1afc-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="d1afc-119">La ventana debe pertenecer a la página del asistente.</span><span class="sxs-lookup"><span data-stu-id="d1afc-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="d1afc-120">Devuelve **false** para permitir que el asistente finalice.</span><span class="sxs-lookup"><span data-stu-id="d1afc-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1afc-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1afc-121">Remarks</span></span>

<span data-ttu-id="d1afc-122">Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT y el procedimiento de cuadro de diálogo debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="d1afc-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="d1afc-123">Versión 5,80.</span><span class="sxs-lookup"><span data-stu-id="d1afc-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="d1afc-124">Si la aplicación devuelve **true** para impedir que un asistente finalice, no tiene ningún control sobre qué ventana de la página recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="d1afc-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="d1afc-125">Las aplicaciones que necesitan detener el final del asistente normalmente deberían hacerlo devolviendo el identificador de la ventana en la página del asistente que va a recibir el foco.</span><span class="sxs-lookup"><span data-stu-id="d1afc-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1afc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1afc-126">Requirements</span></span>



| <span data-ttu-id="d1afc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1afc-127">Requirement</span></span> | <span data-ttu-id="d1afc-128">Value</span><span class="sxs-lookup"><span data-stu-id="d1afc-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1afc-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1afc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d1afc-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d1afc-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d1afc-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1afc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d1afc-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1afc-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d1afc-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1afc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1afc-134"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1afc-134"><dt>Prsht.h</dt></span></span> </dl> |



 

