---
title: Mensaje de LB_SETTOPINDEX (Winuser. h)
description: Garantiza que el elemento especificado en un cuadro de lista está visible.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- LB_SETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150900"
---
# <a name="lb_settopindex-message"></a><span data-ttu-id="be021-104">\_Mensaje lb SETTOPINDEX</span><span class="sxs-lookup"><span data-stu-id="be021-104">LB\_SETTOPINDEX message</span></span>

<span data-ttu-id="be021-105">Garantiza que el elemento especificado en un cuadro de lista está visible.</span><span class="sxs-lookup"><span data-stu-id="be021-105">Ensures that the specified item in a list box is visible.</span></span>

## <a name="parameters"></a><span data-ttu-id="be021-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be021-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be021-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be021-108">Índice de base cero del elemento en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="be021-108">The zero-based index of the item in the list box.</span></span>

<span data-ttu-id="be021-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="be021-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="be021-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="be021-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="be021-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="be021-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="be021-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be021-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be021-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="be021-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be021-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be021-114">Return value</span></span>

<span data-ttu-id="be021-115">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="be021-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="be021-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be021-116">Remarks</span></span>

<span data-ttu-id="be021-117">El sistema desplaza el contenido del cuadro de lista para que el elemento especificado aparezca en la parte superior del cuadro de lista o hasta que se alcance el intervalo de desplazamiento máximo.</span><span class="sxs-lookup"><span data-stu-id="be021-117">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="be021-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be021-118">Requirements</span></span>



| <span data-ttu-id="be021-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be021-119">Requirement</span></span> | <span data-ttu-id="be021-120">Value</span><span class="sxs-lookup"><span data-stu-id="be021-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be021-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be021-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be021-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="be021-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be021-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be021-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be021-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="be021-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be021-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be021-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be021-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be021-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be021-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="be021-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be021-128">**LB \_ GETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="be021-128">**LB\_GETTOPINDEX**</span></span>](lb-gettopindex.md)
</dt> </dl>

 

 





