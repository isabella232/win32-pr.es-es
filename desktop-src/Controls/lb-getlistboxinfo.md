---
title: Mensaje de LB_GETLISTBOXINFO (Winuser. h)
description: Obtiene el número de elementos por columna de un cuadro de lista especificado.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- LB_GETLISTBOXINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079269"
---
# <a name="lb_getlistboxinfo-message"></a><span data-ttu-id="c1ef7-104">\_Mensaje lb GETLISTBOXINFO</span><span class="sxs-lookup"><span data-stu-id="c1ef7-104">LB\_GETLISTBOXINFO message</span></span>

<span data-ttu-id="c1ef7-105">Obtiene el número de elementos por columna de un cuadro de lista especificado.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-105">Gets the number of items per column in a specified list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1ef7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1ef7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ef7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1ef7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ef7-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1ef7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1ef7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ef7-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ef7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1ef7-111">Return value</span></span>

<span data-ttu-id="c1ef7-112">El valor devuelto es el número de elementos por columna.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-112">The return value is the number of items per column.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1ef7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1ef7-113">Remarks</span></span>

<span data-ttu-id="c1ef7-114">Este mensaje es equivalente a [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span><span class="sxs-lookup"><span data-stu-id="c1ef7-114">This message is equivalent to [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1ef7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1ef7-115">Requirements</span></span>



| <span data-ttu-id="c1ef7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1ef7-116">Requirement</span></span> | <span data-ttu-id="c1ef7-117">Value</span><span class="sxs-lookup"><span data-stu-id="c1ef7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ef7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1ef7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1ef7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c1ef7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c1ef7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1ef7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1ef7-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1ef7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1ef7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1ef7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1ef7-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1ef7-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ef7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1ef7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ef7-125">**GetListBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="c1ef7-125">**GetListBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





