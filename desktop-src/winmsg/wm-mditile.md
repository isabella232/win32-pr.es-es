---
description: Una aplicación envía el mensaje de MDITILE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI en formato de mosaico.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Mensaje de WM_MDITILE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275350"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="3be89-103">Mensaje de MDITILE de WM \_</span><span class="sxs-lookup"><span data-stu-id="3be89-103">WM\_MDITILE message</span></span>

<span data-ttu-id="3be89-104">Una aplicación envía el mensaje de **\_ MDITILE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI en formato de mosaico.</span><span class="sxs-lookup"><span data-stu-id="3be89-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="3be89-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3be89-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be89-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3be89-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3be89-107">La opción de mosaico.</span><span class="sxs-lookup"><span data-stu-id="3be89-107">The tiling option.</span></span> <span data-ttu-id="3be89-108">Este parámetro puede ser uno de los siguientes valores, combinados opcionalmente con **MDITILE \_ SKIPDISABLED** para evitar que las ventanas secundarias MDI deshabilitadas se coloquen en mosaico.</span><span class="sxs-lookup"><span data-stu-id="3be89-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="3be89-109">Value</span><span class="sxs-lookup"><span data-stu-id="3be89-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="3be89-110">Significado</span><span class="sxs-lookup"><span data-stu-id="3be89-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="3be89-111"><dt>**MDITILE \_**</dt> <dt>0x0001</dt> horizontal</span><span class="sxs-lookup"><span data-stu-id="3be89-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="3be89-112">Mosaicos ventanas horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="3be89-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="3be89-113"><dt>**MDITILE \_**</dt> <dt>0x0000</dt> vertical</span><span class="sxs-lookup"><span data-stu-id="3be89-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="3be89-114">Mosaicos ventanas verticalmente.</span><span class="sxs-lookup"><span data-stu-id="3be89-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="3be89-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3be89-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3be89-116">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3be89-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be89-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3be89-117">Return value</span></span>

<span data-ttu-id="3be89-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3be89-118">Type: **BOOL**</span></span>

<span data-ttu-id="3be89-119">Si el mensaje se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="3be89-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="3be89-120">Si se produce un error en el mensaje, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="3be89-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be89-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3be89-121">Requirements</span></span>



| <span data-ttu-id="3be89-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be89-122">Requirement</span></span> | <span data-ttu-id="3be89-123">Value</span><span class="sxs-lookup"><span data-stu-id="3be89-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be89-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3be89-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3be89-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3be89-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3be89-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3be89-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3be89-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3be89-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3be89-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3be89-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be89-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3be89-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be89-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3be89-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3be89-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3be89-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3be89-132">**MDICASCADE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="3be89-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="3be89-133">**MDIICONARRANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="3be89-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="3be89-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="3be89-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3be89-135">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="3be89-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




