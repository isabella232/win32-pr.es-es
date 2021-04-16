---
title: Mensaje de TB_SETBUTTONSIZE (commctrl. h)
description: Establece el tamaño de los botones de una barra de herramientas.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658204"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="b1ed2-104">\_Mensaje SETBUTTONSIZE TB</span><span class="sxs-lookup"><span data-stu-id="b1ed2-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="b1ed2-105">Establece el tamaño de los botones de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1ed2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1ed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ed2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1ed2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ed2-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b1ed2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1ed2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ed2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el ancho, en píxeles, de los botones.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="b1ed2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el alto, en píxeles, de los botones.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ed2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1ed2-112">Return value</span></span>

<span data-ttu-id="b1ed2-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ed2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1ed2-114">Remarks</span></span>

<span data-ttu-id="b1ed2-115">**TB \_** Por lo general, se debe llamar a SETBUTTONSIZE después de agregar botones.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="b1ed2-116">Use [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) para establecer los anchos máximo y mínimo permitidos para los botones antes de agregarlos.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="b1ed2-117">Use **TB \_ SETBUTTONSIZE** para establecer el tamaño real de los botones.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="b1ed2-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b1ed2-118">Examples</span></span>

<span data-ttu-id="b1ed2-119">En el siguiente código de ejemplo se establece el ancho de los botones en 80 píxeles y el alto en 30 píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1ed2-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="b1ed2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1ed2-120">Requirements</span></span>



| <span data-ttu-id="b1ed2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ed2-121">Requirement</span></span> | <span data-ttu-id="b1ed2-122">Value</span><span class="sxs-lookup"><span data-stu-id="b1ed2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ed2-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1ed2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ed2-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b1ed2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1ed2-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1ed2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ed2-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1ed2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1ed2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1ed2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1ed2-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ed2-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

