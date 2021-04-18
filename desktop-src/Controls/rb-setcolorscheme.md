---
title: Mensaje de RB_SETCOLORSCHEME (commctrl. h)
description: Establece la información de la combinación de colores para el control rebar.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534348"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="79520-104">Mensaje de SETCOLORSCHEME de RB \_</span><span class="sxs-lookup"><span data-stu-id="79520-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="79520-105">Establece la información de la combinación de colores para el control rebar.</span><span class="sxs-lookup"><span data-stu-id="79520-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="79520-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79520-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79520-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79520-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="79520-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="79520-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="79520-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79520-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79520-110">Puntero a una estructura [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contiene la información de la combinación de colores.</span><span class="sxs-lookup"><span data-stu-id="79520-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79520-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79520-111">Return value</span></span>

<span data-ttu-id="79520-112">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="79520-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="79520-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79520-113">Remarks</span></span>

<span data-ttu-id="79520-114">El control rebar usa la información de la combinación de colores al dibujar los elementos 3D en el control y las bandas.</span><span class="sxs-lookup"><span data-stu-id="79520-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="79520-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79520-115">Requirements</span></span>



| <span data-ttu-id="79520-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79520-116">Requirement</span></span> | <span data-ttu-id="79520-117">Value</span><span class="sxs-lookup"><span data-stu-id="79520-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79520-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79520-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79520-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79520-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79520-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79520-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79520-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="79520-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79520-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79520-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79520-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79520-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79520-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="79520-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79520-125">**\_GETCOLORSCHEME RB**</span><span class="sxs-lookup"><span data-stu-id="79520-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 





