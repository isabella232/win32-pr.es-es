---
title: Mensaje de LB_GETITEMDATA (Winuser. h)
description: Obtiene el valor definido por la aplicación asociado al elemento de cuadro de lista especificado.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151056"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="9367d-104">\_Mensaje lb GETITEMDATA</span><span class="sxs-lookup"><span data-stu-id="9367d-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="9367d-105">Obtiene el valor definido por la aplicación asociado al elemento de cuadro de lista especificado.</span><span class="sxs-lookup"><span data-stu-id="9367d-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="9367d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9367d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9367d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9367d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9367d-108">Índice del elemento.</span><span class="sxs-lookup"><span data-stu-id="9367d-108">The index of the item.</span></span>

<span data-ttu-id="9367d-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9367d-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="9367d-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="9367d-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="9367d-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="9367d-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="9367d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9367d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9367d-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9367d-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9367d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9367d-114">Return value</span></span>

<span data-ttu-id="9367d-115">El valor devuelto es el valor asociado al elemento o LB \_ Err si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9367d-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="9367d-116">Si el elemento se encuentra en un cuadro de lista dibujado por el propietario y se creó sin el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , este valor se encontraba en el parámetro *lParam* del mensaje [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) que agregó el elemento al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="9367d-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="9367d-117">De lo contrario, es el valor de *lParam* del mensaje [**lb \_ SETITEMDATA**](lb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9367d-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9367d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9367d-118">Requirements</span></span>



| <span data-ttu-id="9367d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9367d-119">Requirement</span></span> | <span data-ttu-id="9367d-120">Value</span><span class="sxs-lookup"><span data-stu-id="9367d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9367d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9367d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9367d-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9367d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9367d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9367d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9367d-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9367d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9367d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9367d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9367d-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9367d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9367d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9367d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="9367d-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9367d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9367d-129">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="9367d-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="9367d-130">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="9367d-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="9367d-131">**LB \_ SETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="9367d-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 





