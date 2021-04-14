---
title: Mensaje de WM_DELETEITEM (Winuser. h)
description: Se envía al propietario de un cuadro de lista o cuadro combinado cuando se destruye el cuadro de lista o el cuadro combinado o cuando los elementos se quitan mediante el \_ mensaje lb DELETESTRING, lb \_ RESETCONTENT, CB \_ DELETESTRING o CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490366"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="be1e5-104">Mensaje de WM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="be1e5-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="be1e5-105">Se envía al propietario de un cuadro de lista o cuadro combinado cuando se destruye el cuadro de lista o el cuadro combinado o cuando los elementos se quitan mediante el mensaje [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ RESETCONTENT**](cb-resetcontent.md) .</span><span class="sxs-lookup"><span data-stu-id="be1e5-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="be1e5-106">El sistema envía un mensaje de **WM \_ DELETEITEM** para cada elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="be1e5-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="be1e5-107">El sistema envía el mensaje de **WM \_ DELETEITEM** para cualquier elemento de cuadro combinado o cuadro de lista eliminado con datos de elementos distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="be1e5-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="be1e5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be1e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be1e5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be1e5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be1e5-110">Especifica el identificador del control que envió el mensaje de **WM \_ DELETEITEM** .</span><span class="sxs-lookup"><span data-stu-id="be1e5-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="be1e5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be1e5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be1e5-112">Puntero a una estructura [**deleteitemstruct (**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) que contiene información sobre el elemento eliminado de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="be1e5-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be1e5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be1e5-113">Return value</span></span>

<span data-ttu-id="be1e5-114">Una aplicación debe devolver **true** si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="be1e5-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1e5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be1e5-115">Remarks</span></span>

<span data-ttu-id="be1e5-116">Microsoft Windows NT y versiones posteriores: Windows envía un mensaje de **WM \_ DELETEITEM** solo para los elementos eliminados de un cuadro de lista dibujado por el propietario (con el estilo de la lbs de las [**libras \_**](list-box-styles.md) o el tipo [**\_ OwnerDrawVariable**](list-box-styles.md) ) o el cuadro combinado dibujado por el propietario (con el estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="be1e5-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="be1e5-117">Windows 95: Windows envía el mensaje de **WM \_ DELETEITEM** para cualquier elemento de cuadro combinado o cuadro de lista eliminado con datos de elementos distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="be1e5-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="be1e5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be1e5-118">Requirements</span></span>



| <span data-ttu-id="be1e5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be1e5-119">Requirement</span></span> | <span data-ttu-id="be1e5-120">Value</span><span class="sxs-lookup"><span data-stu-id="be1e5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be1e5-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be1e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be1e5-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="be1e5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be1e5-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be1e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be1e5-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="be1e5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be1e5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be1e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be1e5-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be1e5-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be1e5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="be1e5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="be1e5-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="be1e5-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be1e5-129">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="be1e5-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="be1e5-130">**CB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="be1e5-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="be1e5-131">**DELETEITEMSTRUCT (**</span><span class="sxs-lookup"><span data-stu-id="be1e5-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="be1e5-132">**LB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="be1e5-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="be1e5-133">**LB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="be1e5-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





