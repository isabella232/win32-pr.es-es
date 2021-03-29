---
title: Código de notificación de CBEN_DELETEITEM (commctrl. h)
description: Se envía cuando se ha eliminado un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- CBEN_DELETEITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905556"
---
# <a name="cben_deleteitem-notification-code"></a><span data-ttu-id="a8310-105">Código de notificación de CBEN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="a8310-105">CBEN\_DELETEITEM notification code</span></span>

<span data-ttu-id="a8310-106">Se envía cuando se ha eliminado un elemento.</span><span class="sxs-lookup"><span data-stu-id="a8310-106">Sent when an item has been deleted.</span></span> <span data-ttu-id="a8310-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a8310-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a8310-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8310-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8310-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8310-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8310-110">Puntero a una estructura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contiene información sobre el código de notificación y el elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="a8310-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code and the deleted item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8310-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8310-111">Return value</span></span>

<span data-ttu-id="a8310-112">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="a8310-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8310-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8310-113">Requirements</span></span>



| <span data-ttu-id="a8310-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8310-114">Requirement</span></span> | <span data-ttu-id="a8310-115">Value</span><span class="sxs-lookup"><span data-stu-id="a8310-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8310-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8310-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8310-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8310-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8310-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8310-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8310-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8310-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8310-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8310-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8310-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8310-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





