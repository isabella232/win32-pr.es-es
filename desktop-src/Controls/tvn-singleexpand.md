---
title: Código de notificación de TVN_SINGLEEXPAND (commctrl. h)
description: Enviado por un control de vista de árbol con el \_ estilo de SINGLEEXPAND de los televisores cuando el usuario abre o cierra un elemento de árbol con un solo clic del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489635"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="b22a8-105">Código de notificación de SINGLEEXPAND de TVN \_</span><span class="sxs-lookup"><span data-stu-id="b22a8-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="b22a8-106">Enviado por un control de vista de árbol con el estilo de [**\_ SINGLEEXPAND de los televisores**](tree-view-control-window-styles.md) cuando el usuario abre o cierra un elemento de árbol con un solo clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="b22a8-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="b22a8-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b22a8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="b22a8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b22a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22a8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b22a8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b22a8-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="b22a8-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b22a8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b22a8-111">Return value</span></span>

<span data-ttu-id="b22a8-112">Devuelve \_ el valor predeterminado de TVNRET para permitir que se produzca el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b22a8-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="b22a8-113">Para modificar el comportamiento predeterminado, devuelva:</span><span class="sxs-lookup"><span data-stu-id="b22a8-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="b22a8-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b22a8-114">Return code</span></span>                                                                                    | <span data-ttu-id="b22a8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b22a8-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="b22a8-116"><dt>**TVNRET \_ SKIPOLD**</dt></span><span class="sxs-lookup"><span data-stu-id="b22a8-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="b22a8-117">Omitir el procesamiento predeterminado del elemento que se va a anular la selección.</span><span class="sxs-lookup"><span data-stu-id="b22a8-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="b22a8-118"><dt>**TVNRET \_ SKIPNEW**</dt></span><span class="sxs-lookup"><span data-stu-id="b22a8-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="b22a8-119">Omitir el procesamiento predeterminado del elemento que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="b22a8-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="b22a8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b22a8-120">Remarks</span></span>

<span data-ttu-id="b22a8-121">Para omitir el procesamiento predeterminado de los elementos seleccionados y no seleccionados, devuelva TVNRET \_ SKIPOLD y TVNRET \_ SKIPNEW combinándolos con un operador lógico or.</span><span class="sxs-lookup"><span data-stu-id="b22a8-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="b22a8-122">Este código de notificación solo lo envían los controles de vista de árbol que tienen el estilo [**\_ SINGLEEXPAND de TV**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b22a8-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22a8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b22a8-123">Requirements</span></span>



| <span data-ttu-id="b22a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b22a8-124">Requirement</span></span> | <span data-ttu-id="b22a8-125">Value</span><span class="sxs-lookup"><span data-stu-id="b22a8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b22a8-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b22a8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b22a8-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b22a8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b22a8-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b22a8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b22a8-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b22a8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b22a8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b22a8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22a8-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b22a8-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





