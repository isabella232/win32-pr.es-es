---
title: Código de notificación de PSN_KILLACTIVE (Prsht. h)
description: Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha haga clic en el botón Aceptar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996285"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="c06cb-105">Código de notificación de KILLACTIVE de PSN \_</span><span class="sxs-lookup"><span data-stu-id="c06cb-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="c06cb-106">Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha haga clic en el botón Aceptar.</span><span class="sxs-lookup"><span data-stu-id="c06cb-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="c06cb-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c06cb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c06cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c06cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c06cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c06cb-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c06cb-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="c06cb-111">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c06cb-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="c06cb-112">El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.</span><span class="sxs-lookup"><span data-stu-id="c06cb-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06cb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c06cb-113">Return value</span></span>

<span data-ttu-id="c06cb-114">Devuelve **true** para evitar que la página pierda la activación o **false** para permitirlo.</span><span class="sxs-lookup"><span data-stu-id="c06cb-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="c06cb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c06cb-115">Remarks</span></span>

<span data-ttu-id="c06cb-116">Una aplicación controla este código de notificación para validar la información que el usuario ha escrito.</span><span class="sxs-lookup"><span data-stu-id="c06cb-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="c06cb-117">La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación KILLACTIVE de PSN.</span><span class="sxs-lookup"><span data-stu-id="c06cb-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="c06cb-118">No intente agregar, quitar o insertar páginas mientras controla este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c06cb-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="c06cb-119">Si lo hace, tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="c06cb-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="c06cb-120">Para establecer un valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valor de DWL \_ MSGRESULT establecido en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c06cb-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="c06cb-121">El procedimiento del cuadro de diálogo debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="c06cb-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="c06cb-122">Si el procedimiento del cuadro de diálogo establece DWL \_ MSGRESULT en **true**, debería mostrar un cuadro de mensaje para explicar el problema al usuario.</span><span class="sxs-lookup"><span data-stu-id="c06cb-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="c06cb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c06cb-123">Requirements</span></span>



| <span data-ttu-id="c06cb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c06cb-124">Requirement</span></span> | <span data-ttu-id="c06cb-125">Value</span><span class="sxs-lookup"><span data-stu-id="c06cb-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c06cb-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c06cb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c06cb-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c06cb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c06cb-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c06cb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c06cb-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c06cb-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c06cb-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c06cb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c06cb-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c06cb-131"><dt>Prsht.h</dt></span></span> </dl> |



 

