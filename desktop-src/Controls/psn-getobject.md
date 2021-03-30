---
title: Código de notificación de PSN_GETOBJECT (Prsht. h)
description: Se envía por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de pestaña. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079076"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="45eb5-105">PSN \_ código de notificación GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="45eb5-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="45eb5-106">Se envía por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="45eb5-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="45eb5-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="45eb5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="45eb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45eb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45eb5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45eb5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45eb5-110">Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que, en la entrada, contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="45eb5-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="45eb5-111">Si se procesa este código de notificación, debe insertar la información de objeto en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="45eb5-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45eb5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45eb5-112">Return value</span></span>

<span data-ttu-id="45eb5-113">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="45eb5-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="45eb5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45eb5-114">Remarks</span></span>

<span data-ttu-id="45eb5-115">Para proporcionar un objeto, una aplicación debe establecer valores en algunos miembros de la estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="45eb5-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="45eb5-116">El miembro **pObject** debe establecerse en un puntero de objeto válido y el miembro **hResult** debe establecerse en una marca Success.</span><span class="sxs-lookup"><span data-stu-id="45eb5-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="45eb5-117">Para cumplir los estándares del modelo de objetos componentes (COM), aumente siempre el recuento de referencias del objeto al proporcionar un puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="45eb5-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="45eb5-118">Si una aplicación no proporciona un objeto, debe establecer **pObject** en **null** y **hResult** en una marca de error.</span><span class="sxs-lookup"><span data-stu-id="45eb5-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="45eb5-119">Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="45eb5-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45eb5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45eb5-120">Requirements</span></span>



| <span data-ttu-id="45eb5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="45eb5-121">Requirement</span></span> | <span data-ttu-id="45eb5-122">Value</span><span class="sxs-lookup"><span data-stu-id="45eb5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45eb5-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45eb5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="45eb5-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45eb5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45eb5-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45eb5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="45eb5-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45eb5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="45eb5-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45eb5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="45eb5-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="45eb5-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 





