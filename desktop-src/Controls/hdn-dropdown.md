---
title: Código de notificación de HDN_DROPDOWN (commctrl. h)
description: Lo envía un control de encabezado a su elemento primario cuando se hace clic en la flecha de cuadro desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905702"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="729eb-105">\_Código de notificación de desplegable HDN</span><span class="sxs-lookup"><span data-stu-id="729eb-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="729eb-106">Lo envía un control de encabezado a su elemento primario cuando se hace clic en la flecha de cuadro desplegable del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="729eb-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="729eb-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="729eb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="729eb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="729eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="729eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="729eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="729eb-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="729eb-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="729eb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="729eb-111">Return value</span></span>

<span data-ttu-id="729eb-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="729eb-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="729eb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="729eb-113">Remarks</span></span>

<span data-ttu-id="729eb-114">En el ejemplo de la sección sintaxis se muestra cómo el receptor de notificaciones convierte **lParam** para recuperar la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="729eb-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="729eb-115">**WParam** contiene el identificador del control que envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="729eb-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="729eb-116">Este mensaje se envía solo si el estilo HDF \_ SPLITBUTTON está establecido en el elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="729eb-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="729eb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="729eb-117">Requirements</span></span>



| <span data-ttu-id="729eb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="729eb-118">Requirement</span></span> | <span data-ttu-id="729eb-119">Value</span><span class="sxs-lookup"><span data-stu-id="729eb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="729eb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="729eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="729eb-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="729eb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="729eb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="729eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="729eb-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="729eb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="729eb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="729eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="729eb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="729eb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





