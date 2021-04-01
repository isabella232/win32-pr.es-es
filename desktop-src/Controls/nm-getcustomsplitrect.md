---
title: Código de notificación de NM_GETCUSTOMSPLITRECT (commctrl. h)
description: Enviado por un control de botón a su elemento primario para obtener medidas para los dos rectángulos del botón de expansión. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149893"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="ad177-105">Código de notificación de NM \_ GETCUSTOMSPLITRECT</span><span class="sxs-lookup"><span data-stu-id="ad177-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="ad177-106">Enviado por un control de botón a su elemento primario para obtener medidas para los dos rectángulos del botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="ad177-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="ad177-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ad177-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ad177-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad177-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad177-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad177-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad177-110">Un puntero a un [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) para recibir información de rectángulos delimitadores.</span><span class="sxs-lookup"><span data-stu-id="ad177-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="ad177-111">La estructura **NMCUSTOMSPLITRECTINFO** se envía con el código de notificación como una solicitud para que el elemento primario proporcione medidas para los rectángulos del botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="ad177-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad177-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad177-112">Return value</span></span>

<span data-ttu-id="ad177-113">Devuelve [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) para indicar al control de botón que use los valores devueltos en la estructura [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; de lo contrario, devuelve [**CDRF de \_ forma predeterminada**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ad177-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad177-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad177-114">Remarks</span></span>

<span data-ttu-id="ad177-115">Este código de notificación se envía por un control de botón antes de dibujarse.</span><span class="sxs-lookup"><span data-stu-id="ad177-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="ad177-116">El botón debe tener el estilo [**BS \_ SPLITBUTTON**](button-styles.md) o [**BS \_ DEFSPLITBUTTON**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="ad177-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="ad177-117">Si los rectángulos devueltos al control en *lParam* no son válidos, se omiten.</span><span class="sxs-lookup"><span data-stu-id="ad177-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad177-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad177-118">Requirements</span></span>



| <span data-ttu-id="ad177-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad177-119">Requirement</span></span> | <span data-ttu-id="ad177-120">Value</span><span class="sxs-lookup"><span data-stu-id="ad177-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad177-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad177-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ad177-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad177-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad177-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad177-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ad177-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad177-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad177-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad177-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad177-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad177-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





