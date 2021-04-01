---
title: Código de notificación de DTN_USERSTRING (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905062"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="73adf-104">DTN \_ código de notificación de USERSTRING</span><span class="sxs-lookup"><span data-stu-id="73adf-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="73adf-105">Se envía mediante un control de selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control.</span><span class="sxs-lookup"><span data-stu-id="73adf-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="73adf-106">Este código de notificación solo lo envían los controles de DTP que se establecen en el estilo [**\_ APPCANPARSE de DTS**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="73adf-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="73adf-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73adf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="73adf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73adf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73adf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73adf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73adf-110">Puntero a una estructura [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) que contiene información sobre la instancia del código de notificación.</span><span class="sxs-lookup"><span data-stu-id="73adf-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73adf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73adf-111">Return value</span></span>

<span data-ttu-id="73adf-112">El propietario del control debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="73adf-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="73adf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73adf-113">Remarks</span></span>

<span data-ttu-id="73adf-114">El control de este código de notificación permite que el propietario proporcione respuestas personalizadas a las cadenas especificadas por el usuario en el control.</span><span class="sxs-lookup"><span data-stu-id="73adf-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="73adf-115">El propietario debe estar preparado para analizar la cadena de entrada y tomar medidas si es necesario.</span><span class="sxs-lookup"><span data-stu-id="73adf-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="73adf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73adf-116">Requirements</span></span>



| <span data-ttu-id="73adf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="73adf-117">Requirement</span></span> | <span data-ttu-id="73adf-118">Value</span><span class="sxs-lookup"><span data-stu-id="73adf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73adf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73adf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="73adf-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73adf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73adf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73adf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="73adf-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="73adf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73adf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73adf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="73adf-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73adf-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="73adf-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="73adf-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="73adf-126">**DTN \_ USERSTRINGW** (Unicode) y **DTN \_ USERSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="73adf-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 





