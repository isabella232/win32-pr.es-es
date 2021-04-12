---
title: Código de notificación de NM_TOOLTIPSCREATED (barra de herramientas) (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que la barra de herramientas ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Código de notificación de NM_TOOLTIPSCREATED (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489953"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a><span data-ttu-id="8db7f-105">NM \_ TOOLTIPSCREATED (barra de herramientas) código de notificación</span><span class="sxs-lookup"><span data-stu-id="8db7f-105">NM\_TOOLTIPSCREATED (toolbar) notification code</span></span>

<span data-ttu-id="8db7f-106">Notifica a la ventana primaria de una barra de herramientas que la barra de herramientas ha creado un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="8db7f-106">Notifies a toolbar's parent window that the toolbar has created a tooltip control.</span></span> <span data-ttu-id="8db7f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8db7f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8db7f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8db7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db7f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8db7f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8db7f-110">Puntero a una estructura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="8db7f-110">Pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8db7f-111">Return value</span></span>

<span data-ttu-id="8db7f-112">El control de barra de herramientas omite el valor devuelto de este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="8db7f-112">The toolbar control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db7f-113">Requirements</span></span>



| <span data-ttu-id="8db7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db7f-114">Requirement</span></span> | <span data-ttu-id="8db7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="8db7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8db7f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8db7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8db7f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8db7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8db7f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8db7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8db7f-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8db7f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8db7f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8db7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db7f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db7f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





