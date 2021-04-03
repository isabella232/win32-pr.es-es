---
title: Código de notificación de NM_RDBLCLK (vista de lista) (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón secundario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997180"
---
# <a name="nm_rdblclk-list-view-notification-code"></a><span data-ttu-id="57260-105">NM \_ RDBLCLK (vista de lista) código de notificación</span><span class="sxs-lookup"><span data-stu-id="57260-105">NM\_RDBLCLK (list view) notification code</span></span>

<span data-ttu-id="57260-106">Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="57260-106">Sent by a list-view control when the user double-clicks an item with the right mouse button.</span></span> <span data-ttu-id="57260-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="57260-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="57260-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57260-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57260-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57260-110">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="57260-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="57260-111">Puntero a una estructura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="57260-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="57260-112">Los miembros **iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="57260-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57260-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57260-113">Return value</span></span>

<span data-ttu-id="57260-114">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="57260-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="57260-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57260-115">Remarks</span></span>

<span data-ttu-id="57260-116">El miembro **iItem** de *lParam* solo es válido si se ha realizado clic en el icono o la etiqueta de la primera columna.</span><span class="sxs-lookup"><span data-stu-id="57260-116">The **iItem** member of *lParam* is valid only if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="57260-117">Para determinar qué elemento se selecciona cuando tiene lugar un clic en otro lugar de una fila, envíe un mensaje de [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="57260-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="57260-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57260-118">Requirements</span></span>



| <span data-ttu-id="57260-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="57260-119">Requirement</span></span> | <span data-ttu-id="57260-120">Value</span><span class="sxs-lookup"><span data-stu-id="57260-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57260-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57260-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57260-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="57260-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57260-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57260-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57260-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="57260-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57260-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57260-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="57260-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57260-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





