---
description: Una aplicación envía el mensaje de MDIICONARRANGE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Mensaje de WM_MDIICONARRANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497320"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="b58f8-104">Mensaje de MDIICONARRANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="b58f8-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="b58f8-105">Una aplicación envía el mensaje de **\_ MDIICONARRANGE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI minimizadas.</span><span class="sxs-lookup"><span data-stu-id="b58f8-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="b58f8-106">No afecta a las ventanas secundarias que no están minimizadas.</span><span class="sxs-lookup"><span data-stu-id="b58f8-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="b58f8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b58f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b58f8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b58f8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b58f8-109">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b58f8-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b58f8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b58f8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b58f8-111">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b58f8-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b58f8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b58f8-112">Requirements</span></span>



| <span data-ttu-id="b58f8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58f8-113">Requirement</span></span> | <span data-ttu-id="b58f8-114">Value</span><span class="sxs-lookup"><span data-stu-id="b58f8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58f8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58f8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b58f8-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b58f8-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b58f8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58f8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b58f8-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b58f8-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b58f8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b58f8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b58f8-120"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b58f8-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b58f8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b58f8-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="b58f8-122">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b58f8-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b58f8-123">**MDICASCADE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b58f8-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="b58f8-124">**MDITILE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b58f8-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="b58f8-125">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b58f8-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b58f8-126">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="b58f8-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




