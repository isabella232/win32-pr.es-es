---
description: Recupera la fuente con la que el control está dibujando actualmente su texto.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Mensaje de WM_GETFONT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706668"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="48ff9-103">Mensaje de GETFONT de WM \_</span><span class="sxs-lookup"><span data-stu-id="48ff9-103">WM\_GETFONT message</span></span>

<span data-ttu-id="48ff9-104">Recupera la fuente con la que el control está dibujando actualmente su texto.</span><span class="sxs-lookup"><span data-stu-id="48ff9-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="48ff9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48ff9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ff9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48ff9-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48ff9-107">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="48ff9-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="48ff9-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48ff9-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48ff9-109">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="48ff9-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48ff9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48ff9-110">Return value</span></span>

<span data-ttu-id="48ff9-111">Tipo: **HFONT**</span><span class="sxs-lookup"><span data-stu-id="48ff9-111">Type: **HFONT**</span></span>

<span data-ttu-id="48ff9-112">El valor devuelto es un identificador de la fuente utilizada por el control o **null** si el control usa la fuente del sistema.</span><span class="sxs-lookup"><span data-stu-id="48ff9-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="48ff9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48ff9-113">Requirements</span></span>



| <span data-ttu-id="48ff9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="48ff9-114">Requirement</span></span> | <span data-ttu-id="48ff9-115">Value</span><span class="sxs-lookup"><span data-stu-id="48ff9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48ff9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48ff9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48ff9-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="48ff9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="48ff9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48ff9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48ff9-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48ff9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48ff9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48ff9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48ff9-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48ff9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48ff9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="48ff9-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="48ff9-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="48ff9-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="48ff9-124">**WM \_**</span><span class="sxs-lookup"><span data-stu-id="48ff9-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="48ff9-125">**Vista**</span><span class="sxs-lookup"><span data-stu-id="48ff9-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48ff9-126">Windows</span><span class="sxs-lookup"><span data-stu-id="48ff9-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




