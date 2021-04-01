---
title: Código de notificación de LVN_BEGINRDRAG (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se está iniciando una operación de arrastrar y colocar que implique el botón secundario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995973"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="cd7bc-105">Código de notificación de BEGINRDRAG de LVN \_</span><span class="sxs-lookup"><span data-stu-id="cd7bc-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="cd7bc-106">Notifica a la ventana primaria de un control de vista de lista que se está iniciando una operación de arrastrar y colocar que implique el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="cd7bc-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cd7bc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cd7bc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd7bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd7bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7bc-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="cd7bc-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="cd7bc-111">El miembro **iItem** identifica el elemento que se está arrastrando y los demás miembros son cero.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7bc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd7bc-112">Return value</span></span>

<span data-ttu-id="cd7bc-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7bc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd7bc-114">Requirements</span></span>



| <span data-ttu-id="cd7bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7bc-115">Requirement</span></span> | <span data-ttu-id="cd7bc-116">Value</span><span class="sxs-lookup"><span data-stu-id="cd7bc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7bc-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd7bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7bc-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cd7bc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd7bc-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd7bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7bc-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd7bc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd7bc-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd7bc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd7bc-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd7bc-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





