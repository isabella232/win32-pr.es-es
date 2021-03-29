---
title: Mensaje de TB_SETCOLORSCHEME (commctrl. h)
description: Establece la información de la combinación de colores para el control de barra de herramientas.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905590"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="2049b-104">\_Mensaje SETCOLORSCHEME TB</span><span class="sxs-lookup"><span data-stu-id="2049b-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="2049b-105">Establece la información de la combinación de colores para el control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="2049b-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2049b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2049b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2049b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2049b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2049b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2049b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2049b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2049b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2049b-110">Puntero a una estructura [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contiene la información de la combinación de colores.</span><span class="sxs-lookup"><span data-stu-id="2049b-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2049b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2049b-111">Return value</span></span>

<span data-ttu-id="2049b-112">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2049b-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="2049b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2049b-113">Remarks</span></span>

<span data-ttu-id="2049b-114">El control de barra de herramientas usa la información de la combinación de colores al dibujar los elementos 3D en el control.</span><span class="sxs-lookup"><span data-stu-id="2049b-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="2049b-115">Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="2049b-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="2049b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2049b-116">Requirements</span></span>



| <span data-ttu-id="2049b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2049b-117">Requirement</span></span> | <span data-ttu-id="2049b-118">Value</span><span class="sxs-lookup"><span data-stu-id="2049b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2049b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2049b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2049b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2049b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2049b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2049b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2049b-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2049b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2049b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2049b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2049b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2049b-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2049b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2049b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2049b-126">**TB \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="2049b-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





