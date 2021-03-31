---
title: Mensaje de CB_GETDROPPEDWIDTH (Winuser. h)
description: Obtiene el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con la lista \_ desplegable CBS o el estilo de DROPDOWNLIST de CBS \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079370"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="605b2-104">\_Mensaje GETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="605b2-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="605b2-105">Obtiene el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con la lista [**\_ desplegable CBS**](combo-box-styles.md) o el estilo de [**\_ DROPDOWNLIST de CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="605b2-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="605b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="605b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="605b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="605b2-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="605b2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="605b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="605b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="605b2-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="605b2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605b2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="605b2-111">Return value</span></span>

<span data-ttu-id="605b2-112">Si el mensaje se realiza correctamente, el valor devuelto es el ancho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="605b2-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="605b2-113">Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="605b2-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="605b2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="605b2-114">Remarks</span></span>

<span data-ttu-id="605b2-115">De forma predeterminada, el ancho mínimo permitido del cuadro de lista desplegable es cero.</span><span class="sxs-lookup"><span data-stu-id="605b2-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="605b2-116">El ancho del cuadro de lista es el ancho mínimo permitido o el ancho del cuadro combinado, el que sea mayor.</span><span class="sxs-lookup"><span data-stu-id="605b2-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="605b2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605b2-117">Requirements</span></span>



| <span data-ttu-id="605b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="605b2-118">Requirement</span></span> | <span data-ttu-id="605b2-119">Value</span><span class="sxs-lookup"><span data-stu-id="605b2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605b2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="605b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="605b2-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="605b2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="605b2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="605b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="605b2-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="605b2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="605b2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="605b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="605b2-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="605b2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605b2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="605b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605b2-127">**CB \_ SETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="605b2-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





