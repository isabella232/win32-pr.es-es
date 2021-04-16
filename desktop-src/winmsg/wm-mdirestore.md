---
description: Una aplicación envía el mensaje de MDIRESTORE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI de tamaño maximizado o minimizado.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Mensaje de WM_MDIRESTORE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705529"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="5026c-103">Mensaje de MDIRESTORE de WM \_</span><span class="sxs-lookup"><span data-stu-id="5026c-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="5026c-104">Una aplicación envía el mensaje de **\_ MDIRESTORE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI de tamaño maximizado o minimizado.</span><span class="sxs-lookup"><span data-stu-id="5026c-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="5026c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5026c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5026c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5026c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5026c-107">Identificador de la ventana secundaria MDI que se va a restaurar.</span><span class="sxs-lookup"><span data-stu-id="5026c-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="5026c-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5026c-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5026c-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5026c-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5026c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5026c-110">Return value</span></span>

<span data-ttu-id="5026c-111">Tipo: **cero**</span><span class="sxs-lookup"><span data-stu-id="5026c-111">Type: **zero**</span></span>

<span data-ttu-id="5026c-112">El valor devuelto siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="5026c-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5026c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5026c-113">Requirements</span></span>



| <span data-ttu-id="5026c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5026c-114">Requirement</span></span> | <span data-ttu-id="5026c-115">Value</span><span class="sxs-lookup"><span data-stu-id="5026c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5026c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5026c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5026c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5026c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5026c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5026c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5026c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5026c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5026c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5026c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5026c-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5026c-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5026c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5026c-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="5026c-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5026c-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5026c-124">**MDIMAXIMIZE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5026c-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="5026c-125">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5026c-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5026c-126">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="5026c-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




