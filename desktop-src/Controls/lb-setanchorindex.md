---
title: Mensaje de LB_SETANCHORINDEX (Winuser. h)
description: Establece el elemento de delimitador \ 8212; es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos del elemento delimitador hasta el elemento del símbolo de intercalación.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- LB_SETANCHORINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150905"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="0425d-105">\_Mensaje lb SETANCHORINDEX</span><span class="sxs-lookup"><span data-stu-id="0425d-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="0425d-106">Establece el elemento de delimitador, que es el elemento desde el que se inicia una selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="0425d-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="0425d-107">Una selección múltiple abarca todos los elementos del elemento delimitador hasta el elemento del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="0425d-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="0425d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0425d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0425d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0425d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0425d-110">Especifica el índice del nuevo elemento de delimitador.</span><span class="sxs-lookup"><span data-stu-id="0425d-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="0425d-111">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0425d-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="0425d-112">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="0425d-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="0425d-113">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="0425d-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="0425d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0425d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0425d-115">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0425d-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0425d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0425d-116">Return value</span></span>

<span data-ttu-id="0425d-117">Si el mensaje se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="0425d-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="0425d-118">Si se produce un error en el mensaje, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0425d-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="0425d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0425d-119">Requirements</span></span>



| <span data-ttu-id="0425d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0425d-120">Requirement</span></span> | <span data-ttu-id="0425d-121">Value</span><span class="sxs-lookup"><span data-stu-id="0425d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0425d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0425d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0425d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0425d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0425d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0425d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0425d-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0425d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0425d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0425d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0425d-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0425d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0425d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0425d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0425d-129">**LB \_ GETANCHORINDEX**</span><span class="sxs-lookup"><span data-stu-id="0425d-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





