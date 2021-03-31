---
title: Código de notificación de NM_DBLCLK (vista de lista) (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add6af24b4272631be7c2be387a7ffda899469b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904998"
---
# <a name="nm_dblclk-list-view-notification-code"></a><span data-ttu-id="ba034-105">NM \_ DBLCLK (vista de lista) código de notificación</span><span class="sxs-lookup"><span data-stu-id="ba034-105">NM\_DBLCLK (list view) notification code</span></span>

<span data-ttu-id="ba034-106">Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="ba034-106">Sent by a list-view control when the user double-clicks an item with the left mouse button.</span></span> <span data-ttu-id="ba034-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ba034-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ba034-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba034-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba034-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba034-110">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ba034-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="ba034-111">Puntero a una estructura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="ba034-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="ba034-112">Los miembros **iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="ba034-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba034-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba034-113">Return value</span></span>

<span data-ttu-id="ba034-114">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="ba034-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba034-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba034-115">Remarks</span></span>

<span data-ttu-id="ba034-116">El miembro **iItem** de *lParam* solo es válido si se hace clic en el icono o la etiqueta de la primera columna.</span><span class="sxs-lookup"><span data-stu-id="ba034-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="ba034-117">Para determinar qué elemento se selecciona cuando tiene lugar un clic en otro lugar de una fila, envíe un mensaje de [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="ba034-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba034-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba034-118">Requirements</span></span>



| <span data-ttu-id="ba034-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba034-119">Requirement</span></span> | <span data-ttu-id="ba034-120">Value</span><span class="sxs-lookup"><span data-stu-id="ba034-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba034-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba034-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba034-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba034-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba034-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba034-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba034-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba034-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba034-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba034-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba034-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba034-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





