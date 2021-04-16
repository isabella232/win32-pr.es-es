---
title: Mensaje de MCIWNDM_CHANGESTYLES (VFW. h)
description: El \_ mensaje MCIWNDM CHANGESTYLES cambia los estilos usados por la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- Mensaje de MCIWNDM_CHANGESTYLES de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651388"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="c95cd-105">MCIWNDM \_ CHANGESTYLES</span><span class="sxs-lookup"><span data-stu-id="c95cd-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="c95cd-106">El mensaje **MCIWNDM \_ CHANGESTYLES** cambia los estilos usados por la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="c95cd-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="c95cd-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .</span><span class="sxs-lookup"><span data-stu-id="c95cd-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="c95cd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c95cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c95cd-109"><span id="mask"></span><span id="MASK"></span>*máscara*</span><span class="sxs-lookup"><span data-stu-id="c95cd-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="c95cd-110">Máscara que identifica los estilos que pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="c95cd-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="c95cd-111">Esta máscara es el operador OR bit a bit de todos los estilos que se permitirán cambiar.</span><span class="sxs-lookup"><span data-stu-id="c95cd-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="c95cd-112"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="c95cd-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="c95cd-113">Nueva configuración de estilo para la ventana.</span><span class="sxs-lookup"><span data-stu-id="c95cd-113">New style settings for the window.</span></span> <span data-ttu-id="c95cd-114">Especifique cero para que este parámetro desactive todos los estilos identificados en la máscara.</span><span class="sxs-lookup"><span data-stu-id="c95cd-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="c95cd-115">Para obtener una lista de los estilos disponibles, vea la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="c95cd-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c95cd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c95cd-116">Return Value</span></span>

<span data-ttu-id="c95cd-117">Devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c95cd-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c95cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c95cd-118">Requirements</span></span>



| <span data-ttu-id="c95cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c95cd-119">Requirement</span></span> | <span data-ttu-id="c95cd-120">Value</span><span class="sxs-lookup"><span data-stu-id="c95cd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c95cd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c95cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c95cd-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c95cd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c95cd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c95cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c95cd-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c95cd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c95cd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c95cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95cd-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c95cd-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c95cd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c95cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95cd-128">**MCIWndCreate**</span><span class="sxs-lookup"><span data-stu-id="c95cd-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="c95cd-129">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="c95cd-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





