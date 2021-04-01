---
title: Código de notificación de PSN_QUERYINITIALFOCUS (Prsht. h)
description: Enviado por una hoja de propiedades para proporcionar a la página de la hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149940"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="f8a3c-105">Código de notificación de QUERYINITIALFOCUS de PSN \_</span><span class="sxs-lookup"><span data-stu-id="f8a3c-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="f8a3c-106">Enviado por una hoja de propiedades para proporcionar a la página de la hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="f8a3c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a3c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f8a3c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8a3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a3c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8a3c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a3c-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) .</span><span class="sxs-lookup"><span data-stu-id="f8a3c-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="f8a3c-111">Convierta el miembro **lParam** de esta estructura a un tipo **hWnd** para recuperar el identificador del control al que se asignará el foco de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="f8a3c-112">La estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a3c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8a3c-113">Return value</span></span>

<span data-ttu-id="f8a3c-114">Para especificar el control que debe recibir el foco, devuelva el identificador del control.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="f8a3c-115">De lo contrario, devuelve cero y Focus irá al control predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="f8a3c-116">Para establecer el valor devuelto, el procedimiento del cuadro de diálogo debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valor de **DWL \_ MSGRESULT** y devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a3c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8a3c-117">Remarks</span></span>

<span data-ttu-id="f8a3c-118">Una aplicación no debe llamar a la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) mientras controla este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="f8a3c-119">Devuelve el identificador del control que debe recibir el foco y el administrador de la hoja de propiedades controlará el cambio de foco.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="f8a3c-120">\_No se envía el código de notificación PSN QUERYINITIALFOCUS si el administrador de la hoja de propiedades determina que ningún control de la página debe recibir el foco.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="f8a3c-121">Este fragmento de código implementa un controlador simple para PSN \_ QUERYINITIALFOCUS.</span><span class="sxs-lookup"><span data-stu-id="f8a3c-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="f8a3c-122">Solicita que se proporcione el foco inicial al control de ubicación (**\_ Ubicación de IDC**).</span><span class="sxs-lookup"><span data-stu-id="f8a3c-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="f8a3c-123">Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="f8a3c-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8a3c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a3c-124">Requirements</span></span>



| <span data-ttu-id="f8a3c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a3c-125">Requirement</span></span> | <span data-ttu-id="f8a3c-126">Value</span><span class="sxs-lookup"><span data-stu-id="f8a3c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a3c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8a3c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a3c-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8a3c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8a3c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8a3c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a3c-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8a3c-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8a3c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8a3c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a3c-132"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a3c-132"><dt>Prsht.h</dt></span></span> </dl> |



 

