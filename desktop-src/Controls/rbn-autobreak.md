---
title: Mensaje de RBN_AUTOBREAK (commctrl. h)
description: Notifica al elemento primario de un Rebar que aparecerá un salto en la barra. El elemento primario determina si se va a crear la interrupción. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905627"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="9dc54-106">RBN \_ mensaje de AUTOinterrupción</span><span class="sxs-lookup"><span data-stu-id="9dc54-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="9dc54-107">Notifica al elemento primario [de un rebar](rebar-controls.md) que aparecerá un salto en la barra.</span><span class="sxs-lookup"><span data-stu-id="9dc54-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="9dc54-108">El elemento primario determina si se va a crear la interrupción.</span><span class="sxs-lookup"><span data-stu-id="9dc54-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="9dc54-109">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9dc54-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9dc54-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dc54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dc54-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9dc54-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9dc54-112">Puntero a una estructura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="9dc54-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dc54-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dc54-113">Return value</span></span>

<span data-ttu-id="9dc54-114">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="9dc54-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc54-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dc54-115">Remarks</span></span>

<span data-ttu-id="9dc54-116">El valor del miembro **fAutoBreak** de la estructura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indica si debe producirse un salto en el rebar.</span><span class="sxs-lookup"><span data-stu-id="9dc54-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="9dc54-117">Para usar este código de notificación, especifique Comctl32.dll versión 6 del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="9dc54-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="9dc54-118">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9dc54-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc54-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc54-119">Requirements</span></span>



| <span data-ttu-id="9dc54-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc54-120">Requirement</span></span> | <span data-ttu-id="9dc54-121">Value</span><span class="sxs-lookup"><span data-stu-id="9dc54-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc54-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dc54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc54-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9dc54-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9dc54-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dc54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc54-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dc54-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9dc54-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dc54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dc54-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dc54-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





