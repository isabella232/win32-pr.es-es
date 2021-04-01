---
title: Mensaje de CB_SETDROPPEDWIDTH (Winuser. h)
description: Una aplicación envía el \_ mensaje CB SETDROPPEDWIDTH para establecer el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con el \_ estilo desplegable CBS o \_ CBS DROPDOWNLIST.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905238"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="da4c8-104">\_Mensaje SETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="da4c8-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="da4c8-105">Una aplicación envía el mensaje **CB \_ SETDROPPEDWIDTH** para establecer el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con el estilo [**\_ desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="da4c8-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="da4c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da4c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da4c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c8-108">Ancho mínimo permitido del cuadro de lista, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="da4c8-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="da4c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da4c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c8-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="da4c8-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4c8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da4c8-111">Return value</span></span>

<span data-ttu-id="da4c8-112">Si el mensaje se realiza correctamente, el valor devuelto es el nuevo ancho del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="da4c8-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="da4c8-113">Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="da4c8-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="da4c8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da4c8-114">Remarks</span></span>

<span data-ttu-id="da4c8-115">De forma predeterminada, el ancho mínimo permitido del cuadro de lista desplegable es cero.</span><span class="sxs-lookup"><span data-stu-id="da4c8-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="da4c8-116">El ancho del cuadro de lista es el ancho mínimo permitido o el ancho del cuadro combinado, el que sea mayor.</span><span class="sxs-lookup"><span data-stu-id="da4c8-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4c8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da4c8-117">Requirements</span></span>



| <span data-ttu-id="da4c8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4c8-118">Requirement</span></span> | <span data-ttu-id="da4c8-119">Value</span><span class="sxs-lookup"><span data-stu-id="da4c8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4c8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da4c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da4c8-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da4c8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da4c8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da4c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da4c8-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da4c8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da4c8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da4c8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="da4c8-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da4c8-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4c8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="da4c8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4c8-127">**CB \_ GETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="da4c8-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





