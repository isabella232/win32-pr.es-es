---
title: Código de notificación de HDN_BEGINDRAG (commctrl. h)
description: Lo envía un control de encabezado cuando se ha iniciado una operación de arrastre en uno de sus elementos. Este código de notificación solo lo envían los controles de encabezado que se establecen en el estilo de la de HDS \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079304"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="5f096-106">Código de notificación de BEGINDRAG de HDN \_</span><span class="sxs-lookup"><span data-stu-id="5f096-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="5f096-107">Lo envía un control de encabezado cuando se ha iniciado una operación de arrastre en uno de sus elementos.</span><span class="sxs-lookup"><span data-stu-id="5f096-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="5f096-108">Este código de notificación solo lo envían los controles de encabezado que se establecen en el estilo de la de [**HDS \_**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5f096-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="5f096-109">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5f096-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5f096-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f096-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f096-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f096-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f096-112">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el elemento de encabezado que se está arrastrando.</span><span class="sxs-lookup"><span data-stu-id="5f096-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f096-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f096-113">Return value</span></span>

<span data-ttu-id="5f096-114">Para permitir que el control de encabezado Administre automáticamente las operaciones de arrastrar y colocar, devuelva **false**.</span><span class="sxs-lookup"><span data-stu-id="5f096-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="5f096-115">Si el propietario del control realiza manualmente una reordenación de arrastrar y colocar, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="5f096-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f096-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f096-116">Remarks</span></span>

<span data-ttu-id="5f096-117">Un control de encabezado tiene como valor predeterminado la administración automática de la reordenación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="5f096-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="5f096-118">Devolver **true** para indicar que la administración de arrastrar y colocar externa (manual) permite que el propietario del control proporcione servicios personalizados como parte del proceso de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="5f096-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f096-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f096-119">Requirements</span></span>



| <span data-ttu-id="5f096-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f096-120">Requirement</span></span> | <span data-ttu-id="5f096-121">Value</span><span class="sxs-lookup"><span data-stu-id="5f096-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f096-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f096-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f096-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f096-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f096-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f096-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f096-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f096-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f096-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f096-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f096-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f096-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





