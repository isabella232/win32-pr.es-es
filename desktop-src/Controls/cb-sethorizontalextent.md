---
title: Mensaje de CB_SETHORIZONTALEXTENT (Winuser. h)
description: Una aplicación envía el \_ mensaje CB SETHORIZONTALEXTENT para establecer el ancho, en píxeles, por el que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490522"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="46e77-104">\_Mensaje SETHORIZONTALEXTENT CB</span><span class="sxs-lookup"><span data-stu-id="46e77-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="46e77-105">Una aplicación envía el mensaje **CB \_ SETHORIZONTALEXTENT** para establecer el ancho, en píxeles, por el que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable).</span><span class="sxs-lookup"><span data-stu-id="46e77-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="46e77-106">Si el ancho del cuadro de lista es menor que este valor, la barra de desplazamiento horizontal se desplaza horizontalmente por los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="46e77-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="46e77-107">Si el ancho del cuadro de lista es igual o mayor que este valor, la barra de desplazamiento horizontal está oculta o, si el cuadro combinado tiene el [**estilo \_ DISABLENOSCROLL de CBS**](combo-box-styles.md) , deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="46e77-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="46e77-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46e77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e77-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46e77-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46e77-110">Especifica el ancho desplazable del cuadro de lista, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="46e77-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="46e77-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46e77-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46e77-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="46e77-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46e77-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e77-113">Requirements</span></span>



| <span data-ttu-id="46e77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e77-114">Requirement</span></span> | <span data-ttu-id="46e77-115">Value</span><span class="sxs-lookup"><span data-stu-id="46e77-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e77-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46e77-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46e77-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46e77-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46e77-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="46e77-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46e77-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46e77-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46e77-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46e77-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e77-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="46e77-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e77-123">**CB \_ GETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="46e77-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 





