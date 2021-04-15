---
title: Código de notificación de HDN_FILTERCHANGE (commctrl. h)
description: Notifica a la ventana primaria del control de encabezado que los atributos de un filtro de control de encabezado se están modificando o editando. Este código de notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489269"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="244c0-105">Código de notificación de FILTERCHANGE de HDN \_</span><span class="sxs-lookup"><span data-stu-id="244c0-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="244c0-106">Notifica a la ventana primaria del control de encabezado que los atributos de un filtro de control de encabezado se están modificando o editando.</span><span class="sxs-lookup"><span data-stu-id="244c0-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="244c0-107">Este código de notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="244c0-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="244c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="244c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="244c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="244c0-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento de encabezado, incluidos los atributos que están a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="244c0-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244c0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="244c0-111">Return value</span></span>

<span data-ttu-id="244c0-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="244c0-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="244c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="244c0-113">Requirements</span></span>



| <span data-ttu-id="244c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="244c0-114">Requirement</span></span> | <span data-ttu-id="244c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="244c0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="244c0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="244c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="244c0-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="244c0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="244c0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="244c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="244c0-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="244c0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="244c0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="244c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="244c0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="244c0-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="244c0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="244c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244c0-123">**HDM \_ SETFILTERCHANGETIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="244c0-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





