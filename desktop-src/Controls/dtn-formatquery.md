---
title: Código de notificación de DTN_FORMATQUERY (commctrl. h)
description: Enviado por un control de selector de fecha y hora (DTP) para recuperar el tamaño máximo permitido de la cadena que se mostrará en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995980"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="0432b-105">Código de notificación de DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="0432b-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="0432b-106">Enviado por un control de selector de fecha y hora (DTP) para recuperar el tamaño máximo permitido de la cadena que se mostrará en un campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0432b-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="0432b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0432b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0432b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0432b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0432b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0432b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0432b-110">Puntero a una estructura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) que contiene información sobre el campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0432b-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="0432b-111">La estructura contiene una subcadena que define un campo de devolución de llamada y recibe el tamaño máximo permitido de la cadena que se mostrará en el campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0432b-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0432b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0432b-112">Return value</span></span>

<span data-ttu-id="0432b-113">El propietario del control debe calcular el ancho máximo posible del texto que se mostrará en el campo de devolución de llamada, establecer el miembro **szMax** de la estructura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) y devolver cero.</span><span class="sxs-lookup"><span data-stu-id="0432b-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0432b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0432b-114">Remarks</span></span>

<span data-ttu-id="0432b-115">El control de este código de notificación prepara el control para ajustar el tamaño máximo de la cadena que se mostrará en un campo de devolución de llamada determinado.</span><span class="sxs-lookup"><span data-stu-id="0432b-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="0432b-116">Esto permite que el control muestre correctamente el resultado en todo momento, lo que reduce el parpadeo dentro de la pantalla del control.</span><span class="sxs-lookup"><span data-stu-id="0432b-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="0432b-117">(Para obtener más información sobre los campos de devolución de llamada, vea [campos de devolución de llamada](date-and-time-picker-controls.md)).</span><span class="sxs-lookup"><span data-stu-id="0432b-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="0432b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0432b-118">Requirements</span></span>



| <span data-ttu-id="0432b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0432b-119">Requirement</span></span> | <span data-ttu-id="0432b-120">Value</span><span class="sxs-lookup"><span data-stu-id="0432b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0432b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0432b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0432b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0432b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0432b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0432b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0432b-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0432b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0432b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0432b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0432b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0432b-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0432b-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0432b-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0432b-128">**DTN \_ FORMATQUERYW** (Unicode) y **DTN \_ FORMATQUERYA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0432b-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 





