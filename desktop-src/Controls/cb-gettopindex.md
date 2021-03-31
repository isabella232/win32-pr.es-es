---
title: Mensaje de CB_GETTOPINDEX (Winuser. h)
description: Una aplicación envía el \_ mensaje CB GETTOPINDEX para recuperar el índice de base cero del primer elemento visible en la parte de cuadro de lista de un cuadro combinado.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996376"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="fe91e-104">\_Mensaje GETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="fe91e-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="fe91e-105">Una aplicación envía el mensaje **CB \_ GETTOPINDEX** para recuperar el índice de base cero del primer elemento visible en la parte de cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="fe91e-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="fe91e-106">Inicialmente, el elemento con el índice 0 está en la parte superior del cuadro de lista, pero si se ha desplazado el contenido del cuadro de lista, es posible que haya otro elemento en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="fe91e-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe91e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe91e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe91e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe91e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe91e-109">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fe91e-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fe91e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe91e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe91e-111">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fe91e-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe91e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe91e-112">Return value</span></span>

<span data-ttu-id="fe91e-113">Si el mensaje se realiza correctamente, el valor devuelto es el índice del primer elemento visible en el cuadro de lista del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="fe91e-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="fe91e-114">Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="fe91e-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe91e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe91e-115">Requirements</span></span>



| <span data-ttu-id="fe91e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe91e-116">Requirement</span></span> | <span data-ttu-id="fe91e-117">Value</span><span class="sxs-lookup"><span data-stu-id="fe91e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe91e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe91e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe91e-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fe91e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe91e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe91e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe91e-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe91e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe91e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe91e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe91e-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe91e-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe91e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe91e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe91e-125">**CB \_ SETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="fe91e-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 





