---
title: Código de notificación de IPN_FIELDCHANGED (commctrl. h)
description: Se envía cuando el usuario cambia un campo en el control o se mueve de un campo a otro. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079619"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="e051a-105">Código de notificación de FIELDCHANGED de IPN \_</span><span class="sxs-lookup"><span data-stu-id="e051a-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="e051a-106">Se envía cuando el usuario cambia un campo en el control o se mueve de un campo a otro.</span><span class="sxs-lookup"><span data-stu-id="e051a-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="e051a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e051a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e051a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e051a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e051a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e051a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e051a-110">Puntero a una estructura [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) que contiene información sobre la dirección modificada.</span><span class="sxs-lookup"><span data-stu-id="e051a-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="e051a-111">El miembro **iValue** de esta estructura contendrá el valor especificado, aunque esté fuera del intervalo del campo.</span><span class="sxs-lookup"><span data-stu-id="e051a-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="e051a-112">Puede modificar este miembro a cualquier valor que esté dentro del intervalo del campo en respuesta a este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e051a-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e051a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e051a-113">Return value</span></span>

<span data-ttu-id="e051a-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e051a-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e051a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e051a-115">Remarks</span></span>

<span data-ttu-id="e051a-116">Este código de notificación no se envía como respuesta a un mensaje [**\_ SETADDRESS de IPM**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e051a-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e051a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e051a-117">Requirements</span></span>



| <span data-ttu-id="e051a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e051a-118">Requirement</span></span> | <span data-ttu-id="e051a-119">Value</span><span class="sxs-lookup"><span data-stu-id="e051a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e051a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e051a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e051a-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e051a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e051a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e051a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e051a-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e051a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e051a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e051a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e051a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e051a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





