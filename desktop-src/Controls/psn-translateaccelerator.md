---
title: Código de notificación de PSN_TRANSLATEACCELERATOR (Prsht. h)
description: Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado. Proporciona a la página una oportunidad para realizar la traducción del acelerador del teclado privado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656469"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="1c88b-106">\_Código de notificación PSN TRANSLATEACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="1c88b-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="1c88b-107">Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado.</span><span class="sxs-lookup"><span data-stu-id="1c88b-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="1c88b-108">Proporciona a la página una oportunidad para realizar la traducción del acelerador del teclado privado.</span><span class="sxs-lookup"><span data-stu-id="1c88b-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="1c88b-109">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1c88b-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1c88b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c88b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c88b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c88b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c88b-112">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="1c88b-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="1c88b-113">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de la estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1c88b-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="1c88b-114">El miembro **lParam** de la estructura **PSHNOTIFY** es un puntero [**al mensaje del mensaje.**](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="1c88b-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="1c88b-115">Se puede convertir en un tipo **LPMSG** para obtener acceso a los parámetros del mensaje que se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="1c88b-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c88b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c88b-116">Return value</span></span>

<span data-ttu-id="1c88b-117">Devuelve PSNRET \_ MESSAGEHANDLED para indicar que no es necesario ningún procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="1c88b-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="1c88b-118">Devuelve PSNRET \_ NoError para solicitar el procesamiento normal.</span><span class="sxs-lookup"><span data-stu-id="1c88b-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c88b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c88b-119">Remarks</span></span>

<span data-ttu-id="1c88b-120">Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT.</span><span class="sxs-lookup"><span data-stu-id="1c88b-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="1c88b-121">El procedimiento del cuadro de diálogo debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="1c88b-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c88b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c88b-122">Requirements</span></span>



| <span data-ttu-id="1c88b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c88b-123">Requirement</span></span> | <span data-ttu-id="1c88b-124">Value</span><span class="sxs-lookup"><span data-stu-id="1c88b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c88b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c88b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c88b-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1c88b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c88b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c88b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c88b-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c88b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c88b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c88b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c88b-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c88b-130"><dt>Prsht.h</dt></span></span> </dl> |



 

