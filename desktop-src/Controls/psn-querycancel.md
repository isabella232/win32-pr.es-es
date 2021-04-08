---
title: Código de notificación de PSN_QUERYCANCEL (Prsht. h)
description: Indica que el usuario ha cancelado la hoja de propiedades. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996283"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="2141b-105">Código de notificación de QUERYCANCEL de PSN \_</span><span class="sxs-lookup"><span data-stu-id="2141b-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="2141b-106">Indica que el usuario ha cancelado la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2141b-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="2141b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2141b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="2141b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2141b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2141b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2141b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2141b-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2141b-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="2141b-111">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2141b-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="2141b-112">El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.</span><span class="sxs-lookup"><span data-stu-id="2141b-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2141b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2141b-113">Return value</span></span>

<span data-ttu-id="2141b-114">Devuelve **true** para evitar la operación de cancelación o **false** para permitirlo.</span><span class="sxs-lookup"><span data-stu-id="2141b-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="2141b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2141b-115">Remarks</span></span>

<span data-ttu-id="2141b-116">Normalmente, este código de notificación se envía cuando un usuario hace clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="2141b-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="2141b-117">También se envía cuando un usuario hace clic en el botón **X** de la esquina superior derecha de la hoja de propiedades o presiona la tecla escape.</span><span class="sxs-lookup"><span data-stu-id="2141b-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="2141b-118">Una página de hoja de propiedades puede controlar este código de notificación para pedir al usuario que Compruebe la operación de cancelación.</span><span class="sxs-lookup"><span data-stu-id="2141b-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="2141b-119">Para establecer un valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT establecido en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2141b-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="2141b-120">El procedimiento del cuadro de diálogo debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="2141b-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2141b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2141b-121">Requirements</span></span>



| <span data-ttu-id="2141b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2141b-122">Requirement</span></span> | <span data-ttu-id="2141b-123">Value</span><span class="sxs-lookup"><span data-stu-id="2141b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2141b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2141b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2141b-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2141b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2141b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2141b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2141b-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2141b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2141b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2141b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2141b-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2141b-129"><dt>Prsht.h</dt></span></span> </dl> |



 

