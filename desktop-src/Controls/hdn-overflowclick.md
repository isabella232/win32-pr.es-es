---
title: Código de notificación de HDN_OVERFLOWCLICK (commctrl. h)
description: Lo envía un control de encabezado a su elemento primario cuando se hace clic en el botón de desbordamiento del encabezado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905293"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="adc6d-105">Código de notificación de OVERFLOWCLICK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="adc6d-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="adc6d-106">Lo envía un control de encabezado a su elemento primario cuando se hace clic en el botón de desbordamiento del encabezado.</span><span class="sxs-lookup"><span data-stu-id="adc6d-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="adc6d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="adc6d-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="adc6d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="adc6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc6d-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adc6d-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc6d-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que describe el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="adc6d-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="adc6d-111">El proceso de llamada es responsable de la asignación de esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida.</span><span class="sxs-lookup"><span data-stu-id="adc6d-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="adc6d-112">Establezca los miembros de la estructura **NMHDR** , incluido el miembro de *código* que se debe establecer en HDN \_ OVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="adc6d-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="adc6d-113">Establezca el miembro **iItem** de la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) en el índice del primer elemento de encabezado que no esté visible y, por lo tanto, debería mostrarse en un desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="adc6d-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc6d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="adc6d-114">Return value</span></span>

<span data-ttu-id="adc6d-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="adc6d-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="adc6d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="adc6d-116">Remarks</span></span>

<span data-ttu-id="adc6d-117">El receptor de notificaciones convierte **lParam** para recuperar la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="adc6d-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="adc6d-118">**WParam** contiene el identificador del control que envía la notificación.</span><span class="sxs-lookup"><span data-stu-id="adc6d-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="adc6d-119">Este mensaje se envía solo cuando se establece el [**\_ desbordamiento de HDS**](header-control-styles.md) de estilo en el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="adc6d-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc6d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adc6d-120">Requirements</span></span>



| <span data-ttu-id="adc6d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="adc6d-121">Requirement</span></span> | <span data-ttu-id="adc6d-122">Value</span><span class="sxs-lookup"><span data-stu-id="adc6d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adc6d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adc6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="adc6d-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="adc6d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="adc6d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adc6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="adc6d-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="adc6d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="adc6d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adc6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="adc6d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="adc6d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





