---
title: Código de notificación de HDN_ITEMDBLCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM. Solo los controles de encabezado que se establecen en el estilo de los botones de HDS \_ envían este código de notificación.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274547"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="e3e07-106">Código de notificación de ITEMDBLCLICK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="e3e07-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="e3e07-107">Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el control.</span><span class="sxs-lookup"><span data-stu-id="e3e07-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="e3e07-108">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e3e07-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="e3e07-109">Solo los controles de encabezado que se establecen en el estilo de los [**\_ botones de HDS**](header-control-styles.md) envían este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e3e07-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e3e07-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3e07-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e07-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3e07-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e07-112">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e3e07-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e07-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3e07-113">Return value</span></span>

<span data-ttu-id="e3e07-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e3e07-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e07-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3e07-115">Requirements</span></span>



| <span data-ttu-id="e3e07-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e07-116">Requirement</span></span> | <span data-ttu-id="e3e07-117">Value</span><span class="sxs-lookup"><span data-stu-id="e3e07-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e07-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3e07-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e07-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3e07-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3e07-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3e07-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e07-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3e07-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3e07-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3e07-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3e07-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3e07-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e3e07-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e3e07-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e3e07-125">**HDN \_ ITEMDBLCLICKW** (Unicode) y **HDN \_ ITEMDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e3e07-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 





