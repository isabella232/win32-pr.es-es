---
title: Mensaje de CB_SETTOPINDEX (Winuser. h)
description: Una aplicación envía el \_ mensaje CB SETTOPINDEX para asegurarse de que un elemento determinado esté visible en el cuadro de lista de un cuadro combinado.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801238"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="d5173-104">\_Mensaje SETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="d5173-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="d5173-105">Una aplicación envía el mensaje **CB \_ SETTOPINDEX** para asegurarse de que un elemento determinado esté visible en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="d5173-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="d5173-106">El sistema desplaza el contenido del cuadro de lista para que el elemento especificado aparezca en la parte superior del cuadro de lista o hasta que se alcance el intervalo de desplazamiento máximo.</span><span class="sxs-lookup"><span data-stu-id="d5173-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5173-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5173-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5173-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5173-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5173-109">Especifica el índice de base cero del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="d5173-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="d5173-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5173-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5173-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d5173-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5173-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5173-112">Return value</span></span>

<span data-ttu-id="d5173-113">Si el mensaje se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="d5173-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="d5173-114">Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d5173-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5173-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5173-115">Requirements</span></span>



| <span data-ttu-id="d5173-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5173-116">Requirement</span></span> | <span data-ttu-id="d5173-117">Value</span><span class="sxs-lookup"><span data-stu-id="d5173-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5173-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5173-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5173-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5173-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5173-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5173-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5173-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5173-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5173-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5173-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5173-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5173-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5173-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5173-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5173-125">**CB \_ GETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="d5173-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 





