---
title: Código de notificación de PSN_RESET (Prsht. h)
description: Notifica a una página que la hoja de propiedades está a punto de ser destruida. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656489"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="feb66-105">Código de notificación de restablecimiento de PSN \_</span><span class="sxs-lookup"><span data-stu-id="feb66-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="feb66-106">Notifica a una página que la hoja de propiedades está a punto de ser destruida.</span><span class="sxs-lookup"><span data-stu-id="feb66-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="feb66-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="feb66-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="feb66-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="feb66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="feb66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feb66-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="feb66-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb66-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="feb66-111">Return value</span></span>

<span data-ttu-id="feb66-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="feb66-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb66-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="feb66-113">Remarks</span></span>

<span data-ttu-id="feb66-114">Todos los cambios realizados desde el último código de notificación de [ \_ aplicación de PSN](psn-apply.md) se cancelan, excepto en el caso de [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), que no admite ese código de notificación.</span><span class="sxs-lookup"><span data-stu-id="feb66-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="feb66-115">El miembro **lParam** de la estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) señalada por *lParam* se establecerá en **true** si el usuario hizo clic en el botón **X** situado en la esquina superior derecha de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="feb66-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="feb66-116">Será **false** si el usuario hizo clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="feb66-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="feb66-117">La estructura **PSHNOTIFY** contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="feb66-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="feb66-118">Una aplicación puede utilizar este código de notificación como una oportunidad para realizar operaciones de limpieza.</span><span class="sxs-lookup"><span data-stu-id="feb66-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="feb66-119">La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación de restablecimiento de PSN.</span><span class="sxs-lookup"><span data-stu-id="feb66-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="feb66-120">No intente agregar, quitar o insertar páginas mientras controla este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="feb66-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="feb66-121">Si lo hace, tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="feb66-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="feb66-122">No llame a la función [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) al procesar este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="feb66-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb66-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb66-123">Requirements</span></span>



| <span data-ttu-id="feb66-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb66-124">Requirement</span></span> | <span data-ttu-id="feb66-125">Value</span><span class="sxs-lookup"><span data-stu-id="feb66-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="feb66-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feb66-126">Minimum supported client</span></span><br/> | <span data-ttu-id="feb66-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="feb66-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="feb66-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feb66-128">Minimum supported server</span></span><br/> | <span data-ttu-id="feb66-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="feb66-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="feb66-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="feb66-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="feb66-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="feb66-131"><dt>Prsht.h</dt></span></span> </dl> |



 

