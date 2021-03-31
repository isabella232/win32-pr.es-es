---
title: Mensaje de CB_GETCOUNT (Winuser. h)
description: Obtiene el número de elementos en el cuadro de lista de un cuadro combinado.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804165"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="533a1-104">\_Mensaje GETCOUNT de CB</span><span class="sxs-lookup"><span data-stu-id="533a1-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="533a1-105">Obtiene el número de elementos en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="533a1-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="533a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="533a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="533a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="533a1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="533a1-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="533a1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="533a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="533a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="533a1-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="533a1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="533a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="533a1-111">Return value</span></span>

<span data-ttu-id="533a1-112">El valor devuelto es el número de elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="533a1-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="533a1-113">Si se produce un error, es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="533a1-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="533a1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="533a1-114">Remarks</span></span>

<span data-ttu-id="533a1-115">El índice está basado en cero, por lo que el recuento devuelto es uno mayor que el valor de índice del último elemento.</span><span class="sxs-lookup"><span data-stu-id="533a1-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="533a1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="533a1-116">Requirements</span></span>



| <span data-ttu-id="533a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="533a1-117">Requirement</span></span> | <span data-ttu-id="533a1-118">Value</span><span class="sxs-lookup"><span data-stu-id="533a1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533a1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="533a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="533a1-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="533a1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="533a1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="533a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="533a1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="533a1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="533a1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="533a1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="533a1-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="533a1-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





