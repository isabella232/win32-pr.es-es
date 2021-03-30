---
title: Código de notificación de CBEN_DRAGBEGIN (commctrl. h)
description: Se envía cuando el usuario comienza a arrastrar la imagen del elemento mostrado en la parte de edición del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150978"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="a6371-105">Código de notificación de DRAGBEGIN de CBEN \_</span><span class="sxs-lookup"><span data-stu-id="a6371-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="a6371-106">Se envía cuando el usuario comienza a arrastrar la imagen del elemento mostrado en la parte de edición del control.</span><span class="sxs-lookup"><span data-stu-id="a6371-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="a6371-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a6371-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6371-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6371-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6371-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6371-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6371-110">Puntero a una estructura [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="a6371-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6371-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6371-111">Return value</span></span>

<span data-ttu-id="a6371-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a6371-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6371-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6371-113">Remarks</span></span>

<span data-ttu-id="a6371-114">Si la aplicación receptora implementa la funcionalidad de arrastrar y colocar del control, la aplicación comenzará la operación de arrastrar y colocar en respuesta a este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="a6371-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6371-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6371-115">Requirements</span></span>



| <span data-ttu-id="a6371-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6371-116">Requirement</span></span> | <span data-ttu-id="a6371-117">Value</span><span class="sxs-lookup"><span data-stu-id="a6371-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6371-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6371-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6371-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6371-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6371-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6371-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6371-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6371-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6371-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6371-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6371-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6371-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a6371-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a6371-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a6371-125">**CBEN \_ DRAGBEGINW** (Unicode) y **CBEN \_ DRAGBEGINA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a6371-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





