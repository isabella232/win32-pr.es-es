---
title: Mensaje de LB_DELETESTRING (Winuser. h)
description: Elimina una cadena de un cuadro de lista.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905476"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="8e49b-104">\_Mensaje lb DELETESTRING</span><span class="sxs-lookup"><span data-stu-id="8e49b-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="8e49b-105">Elimina una cadena de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="8e49b-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e49b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e49b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e49b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e49b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e49b-108">Índice de base cero de la cadena que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8e49b-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="8e49b-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e49b-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="8e49b-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="8e49b-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="8e49b-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="8e49b-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e49b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e49b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e49b-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8e49b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e49b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e49b-114">Return value</span></span>

<span data-ttu-id="8e49b-115">El valor devuelto es un recuento de las cadenas que permanecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="8e49b-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="8e49b-116">El valor devuelto es LB \_ Err si el parámetro *wParam* especifica un índice mayor que el número de elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="8e49b-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e49b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e49b-117">Remarks</span></span>

<span data-ttu-id="8e49b-118">Si una aplicación crea el cuadro de lista con un estilo dibujado por el propietario pero sin el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) , el sistema envía un mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) al propietario del cuadro de lista para que la aplicación pueda liberar cualquier dato adicional asociado al elemento.</span><span class="sxs-lookup"><span data-stu-id="8e49b-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e49b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e49b-119">Requirements</span></span>



| <span data-ttu-id="8e49b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e49b-120">Requirement</span></span> | <span data-ttu-id="8e49b-121">Value</span><span class="sxs-lookup"><span data-stu-id="8e49b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e49b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e49b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e49b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e49b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e49b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e49b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e49b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e49b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e49b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e49b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e49b-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e49b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e49b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e49b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e49b-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8e49b-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e49b-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="8e49b-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="8e49b-131">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="8e49b-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="8e49b-132">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="8e49b-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





