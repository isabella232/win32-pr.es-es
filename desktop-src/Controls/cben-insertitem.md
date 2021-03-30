---
title: Código de notificación de CBEN_INSERTITEM (commctrl. h)
description: Se envía cuando se inserta un nuevo elemento en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804015"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="a5dfc-105">CBEN \_ código de notificación INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="a5dfc-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="a5dfc-106">Se envía cuando se inserta un nuevo elemento en el control.</span><span class="sxs-lookup"><span data-stu-id="a5dfc-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="a5dfc-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a5dfc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5dfc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5dfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5dfc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5dfc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5dfc-110">Puntero a una estructura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contiene información sobre el código de notificación y el elemento que se insertó.</span><span class="sxs-lookup"><span data-stu-id="a5dfc-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5dfc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5dfc-111">Return value</span></span>

<span data-ttu-id="a5dfc-112">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="a5dfc-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5dfc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5dfc-113">Requirements</span></span>



| <span data-ttu-id="a5dfc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5dfc-114">Requirement</span></span> | <span data-ttu-id="a5dfc-115">Value</span><span class="sxs-lookup"><span data-stu-id="a5dfc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5dfc-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5dfc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5dfc-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5dfc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5dfc-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5dfc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5dfc-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5dfc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5dfc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5dfc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5dfc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5dfc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





