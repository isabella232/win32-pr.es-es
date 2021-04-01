---
title: Código de notificación de LVN_ITEMACTIVATE (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario activa un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151281"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="3a4cb-105">Código de notificación de ITEMACTIVATE de LVN \_</span><span class="sxs-lookup"><span data-stu-id="3a4cb-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="3a4cb-106">Lo envía un control de vista de lista cuando el usuario activa un elemento.</span><span class="sxs-lookup"><span data-stu-id="3a4cb-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="3a4cb-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3a4cb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="3a4cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a4cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a4cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a4cb-110">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3a4cb-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="3a4cb-111">Puntero a una estructura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="3a4cb-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="3a4cb-112">[Versión 4,70](common-control-versions.md) y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3a4cb-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="3a4cb-113">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="3a4cb-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4cb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a4cb-114">Return value</span></span>

<span data-ttu-id="3a4cb-115">La aplicación que recibe este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="3a4cb-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4cb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a4cb-116">Remarks</span></span>

<span data-ttu-id="3a4cb-117">Para obtener los elementos que se van a activar, la aplicación receptora debe usar el mensaje [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) para recuperar el número de elementos que se seleccionan y, a continuación, enviar el mensaje [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) con **LVNI \_ seleccionado** hasta que se hayan recuperado todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="3a4cb-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4cb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a4cb-118">Requirements</span></span>



| <span data-ttu-id="3a4cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a4cb-119">Requirement</span></span> | <span data-ttu-id="3a4cb-120">Value</span><span class="sxs-lookup"><span data-stu-id="3a4cb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4cb-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a4cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4cb-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a4cb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a4cb-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a4cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4cb-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a4cb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a4cb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a4cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a4cb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4cb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





