---
title: Mensaje de CB_DELETESTRING (Winuser. h)
description: Elimina una cadena en el cuadro de lista de un cuadro combinado.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151060"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="0fbc8-104">\_Mensaje DELETESTRING CB</span><span class="sxs-lookup"><span data-stu-id="0fbc8-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="0fbc8-105">Elimina una cadena en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fbc8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fbc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fbc8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fbc8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fbc8-108">Índice de base cero de la cadena que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0fbc8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fbc8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fbc8-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fbc8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fbc8-111">Return value</span></span>

<span data-ttu-id="0fbc8-112">El valor devuelto es un recuento de las cadenas que permanecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="0fbc8-113">Si el parámetro *wParam* especifica un índice mayor que el número de elementos de la lista, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fbc8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fbc8-114">Remarks</span></span>

<span data-ttu-id="0fbc8-115">Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el sistema envía un mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) al propietario del cuadro combinado para que la aplicación pueda liberar cualquier dato adicional asociado al elemento.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbc8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fbc8-116">Requirements</span></span>



| <span data-ttu-id="0fbc8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fbc8-117">Requirement</span></span> | <span data-ttu-id="0fbc8-118">Value</span><span class="sxs-lookup"><span data-stu-id="0fbc8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbc8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fbc8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0fbc8-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fbc8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0fbc8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fbc8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0fbc8-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fbc8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0fbc8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fbc8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fbc8-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fbc8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fbc8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fbc8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fbc8-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0fbc8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0fbc8-127">**CB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="0fbc8-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="0fbc8-128">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="0fbc8-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





