---
title: Código de notificación de LVN_COLUMNCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se hizo clic en un encabezado de columna mientras el control de vista de lista estaba en modo de informe. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078934"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="d729f-105">Código de notificación de COLUMNCLICK de LVN \_</span><span class="sxs-lookup"><span data-stu-id="d729f-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="d729f-106">Notifica a la ventana primaria de un control de vista de lista que se hizo clic en un encabezado de columna mientras el control de vista de lista estaba en modo de informe.</span><span class="sxs-lookup"><span data-stu-id="d729f-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="d729f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d729f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d729f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d729f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d729f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d729f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d729f-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="d729f-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="d729f-111">El miembro **iItem** es-1 y el miembro **iSubItem** identifica la columna.</span><span class="sxs-lookup"><span data-stu-id="d729f-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="d729f-112">Todos los demás miembros son cero.</span><span class="sxs-lookup"><span data-stu-id="d729f-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d729f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d729f-113">Return value</span></span>

<span data-ttu-id="d729f-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d729f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d729f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d729f-115">Remarks</span></span>

<span data-ttu-id="d729f-116">El uso de formatos de control de encabezado como la \_ casilla HDF para modificar el formato de los encabezados de columna en un control de vista de lista hace que el control envíe el código de notificación [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) en lugar de LVN \_ COLUMNCLICK cuando se hace clic en un elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d729f-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="d729f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d729f-117">Requirements</span></span>



| <span data-ttu-id="d729f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d729f-118">Requirement</span></span> | <span data-ttu-id="d729f-119">Value</span><span class="sxs-lookup"><span data-stu-id="d729f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d729f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d729f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d729f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d729f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d729f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d729f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d729f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d729f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d729f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d729f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d729f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d729f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





