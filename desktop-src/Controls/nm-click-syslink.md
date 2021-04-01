---
title: Código de notificación de NM_CLICK (syslink) (commctrl. h)
description: Notifica a la ventana primaria de un control que el usuario ha haga clic en un hipervínculo con el botón primario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Código de notificación de NM_CLICK (syslink), controles de Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151273"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="1a8ab-105">NM \_ click (syslink) código de notificación</span><span class="sxs-lookup"><span data-stu-id="1a8ab-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="1a8ab-106">Notifica a la ventana primaria de un control que el usuario ha haga clic en un hipervínculo con el botón primario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="1a8ab-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="1a8ab-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8ab-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1a8ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a8ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a8ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a8ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a8ab-110">Puntero a una estructura [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="1a8ab-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a8ab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a8ab-111">Return value</span></span>

<span data-ttu-id="1a8ab-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1a8ab-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a8ab-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a8ab-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a8ab-114">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="1a8ab-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1a8ab-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a8ab-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a8ab-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a8ab-116">Requirements</span></span>



| <span data-ttu-id="1a8ab-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a8ab-117">Requirement</span></span> | <span data-ttu-id="1a8ab-118">Value</span><span class="sxs-lookup"><span data-stu-id="1a8ab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8ab-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a8ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1a8ab-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1a8ab-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a8ab-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a8ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1a8ab-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a8ab-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a8ab-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a8ab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a8ab-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a8ab-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a8ab-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a8ab-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a8ab-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1a8ab-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a8ab-127">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="1a8ab-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="1a8ab-128">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="1a8ab-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





