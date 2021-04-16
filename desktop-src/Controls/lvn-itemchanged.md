---
title: Código de notificación de LVN_ITEMCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658418"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="d97e6-105">Código de notificación de LVN \_ ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="d97e6-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="d97e6-106">Notifica a la ventana primaria de un control de vista de lista que un elemento ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d97e6-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="d97e6-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d97e6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d97e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d97e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97e6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d97e6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d97e6-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica el elemento y especifica cuál de sus atributos ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d97e6-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="d97e6-111">Si el miembro **iItem** de la estructura a la que apunta *lParam* es-1, el cambio se ha aplicado a todos los elementos de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d97e6-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97e6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d97e6-112">Return value</span></span>

<span data-ttu-id="d97e6-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d97e6-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d97e6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d97e6-114">Remarks</span></span>

<span data-ttu-id="d97e6-115">Si un control de vista de lista tiene el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) y el usuario selecciona un intervalo de elementos manteniendo presionada la tecla Mayús y haciendo clic en el mouse, \_ no se enviarán los códigos de notificación LVN ITEMCHANGED para cada elemento seleccionado o no seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d97e6-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="d97e6-116">En su lugar, recibirá un solo código de notificación [ \_ ODSTATECHANGED de LVN](lvn-odstatechanged.md) , que indica que un intervalo de elementos ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="d97e6-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97e6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d97e6-117">Requirements</span></span>



| <span data-ttu-id="d97e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d97e6-118">Requirement</span></span> | <span data-ttu-id="d97e6-119">Value</span><span class="sxs-lookup"><span data-stu-id="d97e6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d97e6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d97e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d97e6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d97e6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d97e6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d97e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d97e6-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d97e6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d97e6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d97e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d97e6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d97e6-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





